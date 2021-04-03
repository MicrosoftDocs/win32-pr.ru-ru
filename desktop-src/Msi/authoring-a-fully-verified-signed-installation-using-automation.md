---
description: В следующем примере показано, как заполнить таблицу Мсидигиталцертификате и таблицу Мсидигиталсигнатуре с помощью подпрограммы Visual Basic для приложений (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Создание полностью проверенной подписанной установки с помощью службы автоматизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99267feffac71401f36635c08fa7f9f6598a0c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998278"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Создание полностью проверенной подписанной установки с помощью службы автоматизации

В следующем примере показано, как заполнить [таблицу мсидигиталцертификате](msidigitalcertificate-table.md) и [таблицу мсидигиталсигнатуре](msidigitalsignature-table.md) с помощью подпрограммы Visual Basic для приложений (VBA). Дополнительные сведения о защите пакетов установщик Windows см. в разделе [рекомендации по разработке безопасных установок](guidelines-for-authoring-secure-installations.md).

[**Метод филесигнатуреинфо**](installer-filesignatureinfo.md) Возвращает SafeArray байт. Дополнительные сведения см. в разделе [**тип данных SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray). Данные из этого массива должны быть преобразованы в Юникод, поскольку Visual Basic не позволяет записывать байты непосредственно в файл. Затем [**метод сетстреам**](record-setstream.md) может использовать файл преобразованных данных для записи потоковых данных в указанное поле записи [**объекта записи**](record-object.md). Обратите внимание, что преобразование байтовых данных в Юникод может привести к изменению данных и того, что преобразованные данные должны соответствовать исходным данным для проверки правильности подписи. Автор пакета должен убедиться, что исходные и преобразованные данные совпадают.


```VB
Sub PopulateDigitalSignature()

    Dim Installer As Object
    Dim Database As Object
    Dim x() As Byte
    
    Const szSignedCabinet = "c:\test.cab"
    Const szCertFile = "c:\temp\test.cer"
    Const szDatabase = "c:\test.msi"
        
    Set Installer = CreateObject("WindowsInstaller.Installer")
    
    x = Installer.FileSignatureInfo(szSignedCabinet, 0, msiSignatureInfoCertificate)
    
    Dim fs, ts
    Dim s As String
    Set fs = CreateObject("Scripting.FileSystemObject")
    Set ts = fs.CreateTextFile(szCertFile, True)        'Create a file
    
    s = StrConv(x, vbUnicode)
    ts.Write s
    ts.Close
        
    Set Database = Installer.OpenDatabase(szDatabase, msiOpenDatabaseModeTransact)
    Set ViewCert = Database.OpenView("SELECT * FROM `MsiDigitalCertificate`")
    ViewCert.Execute 0
    Set ViewSig = Database.OpenView("SELECT * FROM `MsiDigitalSignature`")
    ViewSig.Execute 0
    
    Set RecordCert = Installer.CreateRecord(2)
    RecordCert.StringData(1) = "Test"
    RecordCert.SetStream 2, szCertFile
    ViewCert.Modify msiViewModifyInsert, RecordCert
    
    Set RecordSig = Installer.CreateRecord(4)
    RecordSig.StringData(1) = "Media"
    RecordSig.StringData(2) = "1"
    RecordSig.StringData(3) = "Test"
    ViewSig.Modify msiViewModifyInsert, RecordSig
    
    Database.Commit
      fs.DeleteFile(szCertFile)
End Sub
```



 

 
