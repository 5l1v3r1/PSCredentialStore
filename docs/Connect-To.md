# Connect-To

## SYNOPSIS
Connects to the given host using the stored CredentialStoreItem.

## SYNTAX

### Private (Default)
```
Connect-To -RemoteHost <String> [-Identifier <String>] -Type <String> [-Credentials <PSCredential>] [-PassThru]
 [<CommonParameters>]
```

### Shared
```
Connect-To -RemoteHost <String> [-Identifier <String>] -Type <String> [-Credentials <PSCredential>] [-Shared]
 [-Path <String>] [-PassThru] [<CommonParameters>]
```

## DESCRIPTION
Establish a connection to the selected host using a stored CredentialStoreItem.

## EXAMPLES

### BEISPIEL 1
```
Connect-To -RemoteHost "ucs.myside.local" -Type CiscoUcs
```

### BEISPIEL 2
```
Connect-To -RemoteHost "ftp.myside.local" -Type FTP
```

### BEISPIEL 3
```
Connect-To -RemoteHost "fas.myside.local" -Type NetAppFAS
```

### BEISPIEL 4
```
Connect-To -RemoteHost "esx01.myside.local" -Type VMware
```

### BEISPIEL 5
```
Connect-To -RemoteHost "vCenter.myside.local" -Type CisServer
```

### BEISPIEL 6
```
Connect-To -RemoteHost "exchange01.myside.local" -Type ExchangeHTTP
```

### BEISPIEL 7
```
Connect-To -RemoteHost "exchange01.myside.local" -Type ExchangeHTTPS
```

## PARAMETERS

### -Credentials
Use this parameter to bypass the stored credentials.
Without this parameter Connect-To tries to read the
needed credentials from the CredentialStore.
If you provide this parameter you skip this lookup behavior.
So you can use it to enable credentials without preparing any user interaction.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identifier
Defaults to "".
Specify a string, which separates two CredentialStoreItems for the
same hostname.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns the value from the underlying connection type function.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Define a custom path to a shared CredentialStore.

```yaml
Type: String
Parameter Sets: Shared
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteHost
Specify the host, for which you would like to change the credentials.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Shared
Switch to shared mode with this param.
This enforces the command to work with a shared CredentialStore which
can be decrypted across systems.

```yaml
Type: SwitchParameter
Parameter Sets: Shared
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Specify the host type of the target.
Currently implemented targets are: Possible connection values are:
CiscoUcs, FTP, NetAppFAS, VMware, CisServer, ExchangeHTTP, ExchangeHTTPS, SCP.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### [None]
## OUTPUTS

### [None]
## NOTES
- File Name   : Connect-To.ps1
- Author      : Marco Blessing - marco.blessing@googlemail.com
- Requires    :

## RELATED LINKS

[https://github.com/OCram85/PSCredentialStore](https://github.com/OCram85/PSCredentialStore)

