# 没有运行容器, 如何查看docker images里的文件结构


获取镜像ID：使用 docker images 命令列出所有可用的 Docker 镜像，并找到你想要查看的镜像的ID。

导出镜像：使用 docker save 命令将镜像导出为 tar 文件。例如：

docker save -o image.tar <image_id_or_name>
解压缩镜像：使用 tar 命令解压缩导出的 tar 文件。例如：

mkdir /path/to/destination_directory
tar -xvf image.tar -C /path/to/destination_directory

查看文件结构：解压缩后，你将得到一个包含镜像文件的目录。你可以在该目录中使用各种命令来查看文件结构，例如使用 ls 命令来列出文件和文件夹。

ls