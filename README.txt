Instructions for compiling MArchiveBatchTool:

1. Install the .NET SDK:

Windows:    https://dotnet.microsoft.com/download
Linux:      sudo apt install dotnet8

2. Clone the GMWare.M2 repo:

    git clone https://gitlab.com/modmyclassic/sega-mega-drive-mini/marchive-batch-tool
    cd marchive-batch-tool
    git checkout de9931a5

3. Cherry-pick commits for fixing larger file support (resolve conflicts as necessary):

    git cherry-pick 1d142260
    git cherry-pick a1a124ec

3. Run the following command inside the marchive-batch-tool directory:

Windows:    "C:\Program Files\dotnet\dotnet.exe" publish -c Release -r win7-x64 --self-contained true MArchiveBatchTool.sln
Linux:      dotnet publish -c Release -r linux-x64 --self-contained true MArchiveBatchTool.sln

4. Navigate to the "MArchiveBatchTool\bin\Release\netcoreapp2.2\win7-x64" (or "linux-x64") directory, where the compiled program will be.
