# (T-SQL) Turkish Citizenship Verification

### Dependencies:
- Ole Automation enable.
```tsql
sp_configure 'show advanced options', 1;
GO
RECONFIGURE;
GO
sp_configure 'Ole Automation Procedures', 1;
GO
RECONFIGURE;
GO
```
- Chilkat ActiveX
```
https://www.chilkatsoft.com/downloads_ActiveX.asp
```

### Usage:
```tsql
DECLARE @Output bit

EXEC kSql_TurkishCitizenshipVerification 
@IdentificationNumber = '11111111111', 
@FirstName = 'Karcan', 
@LastName = 'Özbal' , 
@BirthYear = 1993, 
@Result = @Output OUTPUT

SELECT @Output as Result
```