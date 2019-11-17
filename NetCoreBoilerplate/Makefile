# get all dependancies
getDeps:
	gem install xcop
	dotnet tool install -g dotnet-format  

# Verify csproj files formatting
validateCsproj:
	xcop $(find . -name '*.csproj')

# Verify csproj files formatting
fixCsproj:
	xcop --fix $(find . -name '*.csproj')

# Verify code formatting and return non-zero exit code if it fails
validateCodeFormatting:
	dotnet-format --check --dry-run

# Fix code formatting
fixCodeFormatting:
	dotnet-format 

# Publish ReadyToRun image for linux-x64
publish:
	dotnet publish -c Release -r linux-x64