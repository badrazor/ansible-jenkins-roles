Role lang/java/oracle-sdk
=========================

Download and install `oracle java sdk`_.

.. ansible:role:: lang/java/oracle-sdk

   :become: No

   :default lang_java_oracle_sdk_server: The download server.
   :default lang_java_oracle_sdk_version: The default java version to install (default: none).

   :param version: The java version number to install (eg. 1.8.0_65)(default: `{{lang_java_oracle_sdk_version}}`.
   :param build: The build number of the version (eg. 17).
   :param platform: The platform to download.
   :param format: The format to download.
   :param prefix: Install prefix (default: :file:`{{install_prefix}}/java`).
   :param server: Server to download from (default: :file:`{{lang.java.oracle_sdk.server}}`)
   :param cache_directory: Where to cache downloaded artifacts for future reuse on play host.

   Values for *platform* are "linux-x64" and "windows-i568". All valid values can be seen at the download page. They
   are part of the archive filename.

   Values for *format* are "tar.gz" and ".Z". Downloading and installing `rpms` or `.exe` is not yet implemented.

   The *prefix* directory needs to exist and writable.

   .. note:: The resulting :envvar:`JAVA_HOME` is :file:`{{prefix}}/jdk{{version}}`

.. _oracle java sdk: http://www.oracle.com/technetwork/java/javase/downloads/index.html
