# Disconnect-From

## SYNOPSIS
Terminates a session established with Connect-To using a CredentialStoreItem.

## SYNTAX

```
Disconnect-From [-RemoteHost] <String> [-Type] <String> [-Force] [<CommonParameters>]
```

## DESCRIPTION
Terminates a session established with Connect-To using a CredentialStoreItem.

## EXAMPLES

### BEISPIEL 1
```
Disconnect-From -RemoteHost "ucs.myside.local" -Type CiscoUcs
```

### BEISPIEL 2
```
Disconnect-From -RemoteHost "ftp.myside.local" -Type FTP
```

### BEISPIEL 3
```
Disconnect-From -RemoteHost "fas.myside.local" -Type NetAppFAS
```

### BEISPIEL 4
```
Disconnect-From -RemoteHost "esx01.myside.local" -Type VMware
```

### BEISPIEL 5
```
Disconnect-From -RemoteHost "esx01.myside.local" -Type VMware -Force:$True
```

### BEISPIEL 6
```
Disconnect-From -RemoteHost "vcenter.myside.local" -Type CisServer
```

### BEISPIEL 7
```
Disconnect-From -RemoteHost "exchange01.myside.local" -Type ExchangeHTTP
```

### BEISPIEL 8
```
Disconnect-From -RemoteHost "exchange01.myside.local" -Type ExchangeHTTPS
```

## PARAMETERS

### -Force
Force the disconnect, even if the disconnect would fail.

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

### -RemoteHost
Specify the remote endpoint, whose session you would like to terminate.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Specify the host type of the target.
Currently implemented targets are: CiscoUcs, FTP, NetAppFAS, VMware,
CisServer, ExchangeHTTP, ExchangeHTTPS, SCP.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
- File Name   : Disconnect-From.ps1
- Author      : Marco Blessing - marco.blessing@googlemail.com
- Requires    :

## RELATED LINKS

[https://github.com/OCram85/PSCredentialStore](https://github.com/OCram85/PSCredentialStore)

