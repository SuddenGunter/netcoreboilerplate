# Verify csproj files formatting
validateCsproj:
	xcop $(find . -name '*.csproj')

# Verify csproj files formatting
fixCsproj:
	xcop --fix $(find . -name '*.csproj')

# Publish ReadyToRun image for linux-x64
publish:
	dotnet publish -c Release -r linux-x64
