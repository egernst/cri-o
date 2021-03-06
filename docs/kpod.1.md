% kpod(1) kpod - Simple management tool for pods and images
% Dan Walsh
# kpod "1" "September 2016" "kpod"
## NAME
kpod - Simple management tool for containers and images

## SYNOPSIS
**kpod**
[**--help**|**-h**]

# DESCRIPTION
kpod is a simple client only tool to help with debugging issues when daemons
such as CRI runtime and the kubelet are not responding or failing. A shared API
layer could be created to share code between the daemon and kpod. kpod does not
require any daemon running. kpod utilizes the same underlying components that
crio uses i.e. containers/image, container/storage, oci-runtime-tool/generate,
runc or any other OCI compatible runtime. kpod shares state with crio and so
has the capability to debug pods/images created by crio.

**kpod [GLOBAL OPTIONS]**

## GLOBAL OPTIONS

**--help, -h**
  Print usage statement

**--version, -v**
  Print the version

## COMMANDS

### images
List images in local storage

### rmi
Removes one or more locally stored images

### tag
Add one or more additional names to locally-stored image

### info
Displays system information

## SEE ALSO
crio(8), crio.conf(5)

## HISTORY
Dec 2016, Originally compiled by Dan Walsh <dwalsh@redhat.com>
