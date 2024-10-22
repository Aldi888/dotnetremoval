#dotnetremoval
#by Aldi

#Check dotnet Installed versions
dotnet --list-runtimes

#Check Installed apps
get-itemproperty hklm:\software\microsoft\windows\currentversion\uninstall\* | Select-Object displayname, UninstallString | where displayname | sort displayname

#if no autocad found or Visual Studio (it's still delivering version 6.0.35 of .net)
#remove below comments and run again

#rm -r 'C:\Program Files\dotnet\shared\Microsoft*' 
#dotnet --list-runtimes #check again (this will generate an error, but is false-positive due to dotnet removal success)
