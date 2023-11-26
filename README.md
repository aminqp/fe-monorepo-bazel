# A monorepo Example using Bazel + Vite + React

This illustration showcases the utilization of federated modules from a Vite bundle. The `host` (React-based) relies on a component made accessible by the `remote` app (React-based) through the use of `Bazel`.

## Install Bazel

Prior to commencing any activities, it is essential to confirm that Bazel has been successfully installed on your device. You can verify the installation status by executing the provided command. This step is crucial to ensure that your device is properly equipped to execute the desired tasks with Bazel.

```shell
$ bazel --version
```
```
bazel 5.0.0
```

You should see some output like that otherwise you need to install it first. To do so, you can use this link [bazel.build](https://bazel.build/install).

If you do not observe the expected output when running the command, it indicates that Bazel is not installed on your device. In such a case, you will need to install it. You can easily accomplish this by following the instructions provided in the following link: [bazel.build](https://bazel.build/install). This resource will guide you through the installation process and help you set up Bazel on your device.

## Install Dependencies
Install `pnpm` as per instructions provided [here](https://pnpm.io/installation).
Run the following command on the root of the project

```shell
pnpm install
```

## Building Apps
On the root of the project run the following command
```shell
pnpm run build:all:bazel
```
It will run the `bazel build build` command on all apps to build them using `Bazel`      
If the process completed successfully, you should observe four new directories in your project.

- bazel-bin
- bazel-fe-monorepo-bazel
- bazel-out
- bazel-testlogs

The build output will be located in the `bazel-bin` directory, with a name identical to that of the app.

## Run Apps
Use the following command to serve the final app
```shell
pnpm run serve:all
```
now you can open a browser and navigate to the `host` to see the application.
- HOST: [localhost:5000](http://localhost:5000/)
- REMOTE: [localhost:5001](http://localhost:5001/)
