# How to publish the GNU MCU Eclipse ARM Embedded GCC binaries?

## Update the Change log

Generally, apart from packing, there should be no local changes compared 
to the original ARM distribution.

Open the `CHANGELOG.txt` file from  
`gnu-mcu-eclipse/arm-none-eabi-gcc-build.git` project git, and copy 
entries to the web git.

In the web git, add new entries to the 
[Change log](https://gnu-mcu-eclipse.github.io/toolchain/arm/change-log/) 
(`pages/toolchain/arm/change-log.md`), grouped by days.

Note: if you missed to update the `CHANGELOG.txt` before starting the build, 
edit the file and rerun the build, it should take only a few minutes to 
recreate the archives with the correct file.

## Edit the build script

Edit the `VERSION` file to refer to the actual release.

## Push the build script git

Push `gnu-mcu-eclipse/arm-none-eabi-gcc-build.git` to GitHub.

Possibly push the helper project too.

## Build

Follow the instructions on the 
[build](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc-build/blob/master/README.md) 
page.

## Prepare a new blog post 

In the web git:

- add a new file to `_posts/arm-none-eabi-gcc/releases`
- name the file like `2018-04-01-arm-none-eabi-gcc-v7-2-1-1-1-released.md`
- name the post like: **GNU MCU Eclipse ARM Embedded GCC v7.2.1-1.1 20180401 released**.
- as `download_url` use the generic `https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases/` 
- update the `date:` field with the current date

If any, close [issues](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/issues) 
on the way. Refer to them as:

- **[Issue:\[#1\]\(...\)]**.

## Update the SHA sums

Copy/paste the build report at the end of the post as:

```console
## Checksums
The SHA-256 hashes for the files are:

4fe99c9122c7f2f84a998640d9b3d3d890a2ae47cbd5469813a3ad015e69bbd7 ?
gnu-mcu-eclipse-arm-none-eabi-gcc-7.2.1-1.1-20180401-0515-centos32.tar.xz

ed6c727b859eed4fcb55aa14bdafd329f71b087877d2eb7438abfec2bb533227 ?
gnu-mcu-eclipse-arm-none-eabi-gcc-7.2.1-1.1-20180401-0515-centos64.tar.xz

578c4525187c498ec0b8255ac46d4177ed3b51b115cb6ca4cd379baa6b70db7a ?
gnu-mcu-eclipse-arm-none-eabi-gcc-7.2.1-1.1-20180401-0515-win32.zip

fd9573d0b9e89d87b9bf7f237955bbeba206a93c6cecc2fc3996458798d7a05b ?
gnu-mcu-eclipse-arm-none-eabi-gcc-7.2.1-1.1-20180401-0515-win64.zip

```

## Update the Web

- commit the `gnu-mcu-eclipse.github.io-source` project; use a message 
like **GNU MCU Eclipse ARM Embedded GCC v7.2.1-1.1 released**
- wait for the Travis build to complete; occasionally links to not work,
 and might need to restart the build.
- remember the post URL, since it must be updated in the release page

Note: initially the link to binaries points to the parent releases folder, 
otherwise Travis will complain and do not publish the site to 
`gnu-mcu-eclipse.github.io`.

## Create a new GitHub release

- go to the [GitHub Releases](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases) page
- click **Draft a new release**
- name the tag like **v7.2.1-1.1** (mind the dash in the middle!)
- name the release like **GNU MCU Eclipse ARM Embedded GCC v7.2.1-1.1 20180401** 
(mind the dash and the space)
- as description
  - add a downloads badge like `[![Github Releases (by Release)](https://img.shields.io/github/downloads/gnu-mcu-eclipse/arm-none-eabi-gcc/v7.2.1-1.1/total.svg)]()`; use empty URL for now
  - copy the first paragraph from the Web release page
- add a link to the Web page `[Continue reading »]()`; use an empty URL for now
- get URL from web and update the above links
- **attach binaries** and SHA (drag and drop from the archives folder will do it)
- click the **Publish Release** button

Note: at this moment the system should send a notification to all clients watching this project.

## Update the web link 

In the web git:

- `download_url: https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases/tag/v7.2.1-1.1`
- use something like `v7.2.1-1.1 update link` as message

## Share on Facebook

- go to the new post and follow the Share link.
- DO NOT select **On your own Timeline**, but **On a Page you manage**
- select GNU MCU Eclipse
- posting as GNU MCU Eclipse
- click **Post to Facebook**
- check the post in the [Facebook page](https://www.facebook.com/gnu-mcu-eclipse)

