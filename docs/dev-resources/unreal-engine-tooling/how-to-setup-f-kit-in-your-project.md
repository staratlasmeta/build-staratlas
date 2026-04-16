# How To Setup F-Kit in Your Project

* Open Epic Games Launcher and launch your installed version of Unreal Engine

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-01-image.png" alt=""><figcaption></figcaption></figure>

* Create a new project and select C++ as project template

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-02-image.png" alt=""><figcaption></figcaption></figure>

* Close the editor and open the folder where the Project is located (e.g., `C:\UnrealEngine\SampleProject`
* Create a new `Plugins` folder at the root directory

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-03-image.png" alt=""><figcaption></figcaption></figure>

* Copy your plugin within the `Plugins` directory

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-04-image.png" alt=""><figcaption></figcaption></figure>

* Right-click `.uproject` file located at the root and select `Generate Visual Studio project files`

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-05-image.png" alt=""><figcaption></figcaption></figure>

* Double-click `.sln` file and open the project solution with your C++ IDE (Rider or Visual Studio)
* Open the file located under `Source/<ProjectName>/<ProjectName>.build.cs`

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-06-image.png" alt=""><figcaption></figcaption></figure>

* Addj to `PublicDependencyModuleNames` the plugin module name you want to use in C++. In our case the module we want to use is `Foundation`

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-07-image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-08-image.png" alt=""><figcaption></figcaption></figure>

* Open the `.uproject` file

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-09-image.png" alt=""><figcaption></figcaption></figure>

* Add the plugin name you want to use for your project

<figure><img src="/images/docs-assets/how-to-setup-f-kit-in-your-project-10-image.png" alt=""><figcaption></figcaption></figure>

* Close your IDE and generate project files again. Right-click `.uproject` file on the root directory and `select Generate Visual Studio project files`
* Open your project solution `.sln`
* You can now start using your plugin in C++
