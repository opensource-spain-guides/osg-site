# Opensource Spain Guilds (OSG)

An open-source collection of guides and resources for living and working in Spain: visas, taxes, and daily life tips.

## Project Structure

The project is built using [MkDocs](https://mkdocs.org/) with the [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) theme. The site is designed to be easily maintained and updated by anyone interested in contributing to the project.

### Directory Overview:

- `/docs`: Contains all markdown files for documentation (guides and information).

## Local Development

To get started with local development, follow these steps:

### **1. Build the Docker Image**

This project is Dockerized, meaning you can easily build and run the project in a containerized environment. To build the Docker image, run the following command in your terminal:

```bash
docker build -t osg-site .
```

This command will create an image named `osg-site` based on the Dockerfile in the root directory. The image contains all the dependencies needed to run the site locally.

### **2. Run the Container with Volume Mounting**

Once the Docker image is built, run the following command to start the container and mount your current directory into the container. This allows you to make live changes to the code on your local machine:

```bash
docker run -it --rm -p 8000:8000 -v ${PWD}:/app osg-site
```

After running this command, you can visit `http://localhost:8000` in your browser to view the site. Any changes you make to the documentation files will be reflected in real-time.

### **3. Editing Code**

Once the container is running, you can start editing files in the `/docs` folder. Any changes you make will be automatically reflected on the site because of the volume mount (`-v ${PWD}:/app`). This allows you to make quick edits to the guides without rebuilding or restarting the container.

### **4. Stopping the Container**

When you're done with local development, you can stop the container by simply pressing Ctrl+C in your terminal. Since the `--rm` flag was used, the container will be removed automatically once stopped.

## Contributing

We welcome contributions from anyone interested in helping others navigate the process of moving to and living in Spain. To contribute:

1. Fork the repository.
2. Create a new branch for your changes (`git checkout -b my-feature-branch`).
3. Make your changes to the documentation or code.
4. Commit your changes (`git commit -am 'Add new guide for digital nomad visa'`).
5. Push your changes to your forked repository (`git push origin my-feature-branch`).
6. Create a pull request to merge your changes into the main branch of the original repository.

Please ensure that your contributions adhere to the style and guidelines established in the project.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contact

If you have any questions or suggestions, feel free to reach out via [GitHub issues](https://github.com/opensource-spain-guides/osg-site/issues) or open a pull request to improve the documentation!