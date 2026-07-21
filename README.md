# Download and Embed WSIs from the GDC

### Prerequisites

Download and install the [GDC Data Transfer Tool](https://gdc.cancer.gov/access-data/gdc-data-transfer-tool).

## Download Data

As the WSIs are large files, we rely on the GDC Data Transfer Tool to fetch data using the GDC API given a manifest file of slides to download:
1. Prepare the manifest file: we do this programmatically in [notebooks](./notebooks)
2. Download the data:
    ```bash
    gdc-client download \
    --manifest manifests/manifest.txt \
    --log-file download.log \
    --dir /path/to/save/data # < make sure this directory exists before you start the download
    ```
3. Extract and cleanup data: TODO
