<div>
<img align="left" style="margin: 0px 15px 0px 0px;" src="io.gitlab.Lycanite.Arachnotron.png" alt="Arachnotron Icon" />

# Arachnotron on Flatpak
### &nbsp;

</div>
<p>&nbsp;</p>

This project contains files to build [Arachnotron](https://nephrite.uk/arachnotron) as a Flatpak app.

The app include [GZDoom](https://zdoom.org/) engine to run WADs and files.

## How to build the app

### 1 - Prepare the environment
Ensure you have the following commands installed on your system:
- `git`
- `flatpak`
- `flatpak-builder`

Ensure you have the `flathub` repo enabled:

```shell
$ flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

Clone this project on your computer:

```shell
$ git clone https://github.com/mbugni/ArachnotronFlatpak.git
```

### 2 - Build and install the app
From the project directory run the command:

```shell
$ sudo flatpak-builder --verbose --install --install-deps-from=flathub --force-clean build \
  io.gitlab.Lycanite.Arachnotron.yaml
```

See [flatpak documentation](https://docs.flatpak.org/) for more info.

The first build can take a while (15 minutes or more), it depends on your machine performances. It compile and install the app, making it available for all users in your system.

### 3 - Run the app
You can run the Arachnotron launching it from your favorite desktop, or manually by using the `flatpak` command:

```shell
$ flatpak run io.gitlab.Lycanite.Arachnotron
```

#### Tips
- Select the `GZDoom` engine from the `/app/bin` folder
- Put data files in `~/var/app/io.gitlab.Lycanite.Arachnotron/data`

#### GZDoom options
 GZDoom engine defaults are in file `~/.var/app/io.gitlab.Lycanite.Arachnotron/.config/gzdoom/gzdoom.ini`
