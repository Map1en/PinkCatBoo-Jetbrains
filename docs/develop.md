## IntelliJ IDEA Theme Development Environment Setup

### 1. **Plugin DevKit** plugin is installed and enabled in IntelliJ IDEA.

### 2. IntelliJ Platform SDK is configured.

#### IDE and Java Versions

Java version must be set depending on the target platform version.

**2024.2+: Java 21**

#### Add JDK

1. Go to **File | Project Structure | Platform Settings | SDKs**.

2. Click the **Add button (+)**.

3. If you have the required JDK installation on your machine, and it is detected, select it from the **Detected SDKs** list. If your JDK is not detected, select the **Add JDK...** option and choose the installation folder.

4. If the required JDK is not installed on your machine, the simplest option is using **Download JDK...** and choosing the distribution options.

5. Click the **Apply** button.

The second step is adding IntelliJ Platform Plugin SDK that will use the JDK configured in the first step.

#### Add IntelliJ Platform Plugin SDK

1. Go to **File | Project Structure | Platform Settings | SDKs**.

2. Click the **Add button (+)**.

3. Select the **Add IntelliJ Platform Plugin SDK...** option.

4. Choose the installation folder of the IDE downloaded previously (on macOS, select application icon in `/Applications/`).

5. In the **Select Internal Java Platform** dialog, select the JDK configured in the previous step and click **OK** button.

6. In the added SDK, specify the **Sandbox Home** directory.

7. If debugging is required, select the **Sourcepath** tab, click the **Add button (+)** and select the root folder of the checked-out sources.

8. Click the **Apply** button.

### Add Plugin Run Configuration

1. Go to **Run | Edit Configurations....**

2. Click the **Add New Configuration... button (+)** and select the **Plugin** type.

3. Provide the configuration **Name**, e.g., `Run Theme`.

4. Ensure that **Use classpath of module** specifies the current theme plugin module.

5. Click the **Apply** button.

**Reference:**

* [Developing a Theme](https://plugins.jetbrains.com/docs/intellij/developing-themes.html)