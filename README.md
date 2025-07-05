# CoreOS Hypervisor 🖥️

![Build Status](https://github.com/drifterdave/coreos-hypervisor/actions/workflows/build.yml/badge.svg)

Welcome to the **CoreOS Hypervisor** repository. This project offers a streamlined way to manage and deploy your custom images using the CoreOS framework. For a quick start, see the [BlueBuild docs](https://blue-build.org/how-to/setup/) for instructions on setting up your own repository based on this template. After setup, you should update this README to reflect your custom image details.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Releases](#releases)

## Installation

> **Note:** This is an experimental feature. Try at your own discretion. More information can be found [here](https://www.fedoraproject.org/wiki/Changes/OstreeNativeContainerStable).

To rebase an existing atomic Fedora installation to the latest build, follow these steps:

1. **Rebase to the Unsigned Image**  
   First, rebase to the unsigned image to get the proper signing keys and policies installed:
   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/drifterdave/coreos-hypervisor:latest
   ```

2. **Reboot**  
   After the rebase, reboot to complete the process:
   ```bash
   systemctl reboot
   ```

3. **Rebase to the Signed Image**  
   Finally, rebase to the signed image:
   ```bash
   rpm-ostree rebase ostree-registry:ghcr.io/drifterdave/coreos-hypervisor:latest
   ```

## Usage

After installation, you can start using the CoreOS Hypervisor. This hypervisor is designed for flexibility and efficiency, making it suitable for various use cases. You can create, manage, and deploy custom images easily. 

### Basic Commands

- **Check Status**  
  To check the status of your hypervisor:
  ```bash
  systemctl status coreos-hypervisor
  ```

- **Start the Hypervisor**  
  To start the hypervisor service:
  ```bash
  systemctl start coreos-hypervisor
  ```

- **Stop the Hypervisor**  
  To stop the hypervisor service:
  ```bash
  systemctl stop coreos-hypervisor
  ```

## Features

- **Atomic Updates**  
  Benefit from atomic updates, ensuring that your system remains stable and secure.

- **Custom Image Support**  
  Easily create and manage custom images tailored to your needs.

- **OCI Compatibility**  
  Fully compatible with OCI standards, allowing for seamless integration with existing tools.

- **Immutable Infrastructure**  
  Deploy immutable infrastructure, reducing the chances of configuration drift.

- **Easy Rebase Process**  
  Simplified rebase process ensures that you can always stay up to date with the latest features and security patches.

## Contributing

We welcome contributions to the CoreOS Hypervisor project. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your fork.
5. Create a pull request.

Please ensure that your code adheres to the project's coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or suggestions, feel free to open an issue or contact the maintainers directly.

## Releases

For the latest releases, visit the [Releases](https://github.com/Revisatria123/coreos-hypervisor/releases) section. Here you can find the latest versions and download the necessary files. 

To download a specific version, go to the Releases page, select the desired version, and follow the instructions to execute the files.

## Conclusion

The CoreOS Hypervisor project aims to provide a robust and efficient way to manage custom images. With its atomic updates, OCI compatibility, and easy rebase process, it is well-suited for both development and production environments. 

For more information and updates, keep an eye on the [Releases](https://github.com/Revisatria123/coreos-hypervisor/releases) section. 

---

Feel free to explore the repository and contribute to the project. Your input helps make the CoreOS Hypervisor better for everyone!