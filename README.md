# Disk raw data manager libary

A simple C# library.

A few call allows you to read e write raw data on a DISK.

## Example of reading

```csharp
   DISK.SafeStreamManager myStream;
   
   string phyd = "\\\\.\\PHYSICALDRIVE1" //usually  "\\\\.\\PHYSICALDRIVE0" is C:
   
   myStream = DISK.CreateStream(phyd, FileAccess.Read);
   
   byte[] firstBlock = new byte[512];
   
   firstBlock = DISK.ReadBytes(0, 512, myStream);
   
   DISK.DropStream(myStream);
   



