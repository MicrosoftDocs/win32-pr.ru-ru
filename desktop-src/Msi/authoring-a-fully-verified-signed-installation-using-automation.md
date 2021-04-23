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
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a><span data-ttu-id="a7d5d-103">Создание полностью проверенной подписанной установки с помощью службы автоматизации</span><span class="sxs-lookup"><span data-stu-id="a7d5d-103">Authoring a Fully Verified Signed Installation Using Automation</span></span>

<span data-ttu-id="a7d5d-104">В следующем примере показано, как заполнить [таблицу мсидигиталцертификате](msidigitalcertificate-table.md) и [таблицу мсидигиталсигнатуре](msidigitalsignature-table.md) с помощью подпрограммы Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="a7d5d-104">The following sample demonstrates how to populate the [MsiDigitalCertificate table](msidigitalcertificate-table.md) and [MsiDigitalSignature table](msidigitalsignature-table.md) by using a Visual Basic for Applications (VBA) subroutine.</span></span> <span data-ttu-id="a7d5d-105">Дополнительные сведения о защите пакетов установщик Windows см. в разделе [рекомендации по разработке безопасных установок](guidelines-for-authoring-secure-installations.md).</span><span class="sxs-lookup"><span data-stu-id="a7d5d-105">For more information about securing Windows Installer packages see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md).</span></span>

<span data-ttu-id="a7d5d-106">[**Метод филесигнатуреинфо**](installer-filesignatureinfo.md) Возвращает SafeArray байт.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-106">The [**FileSignatureInfo method**](installer-filesignatureinfo.md) returns a SAFEARRAY of bytes.</span></span> <span data-ttu-id="a7d5d-107">Дополнительные сведения см. в разделе [**тип данных SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="a7d5d-107">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span> <span data-ttu-id="a7d5d-108">Данные из этого массива должны быть преобразованы в Юникод, поскольку Visual Basic не позволяет записывать байты непосредственно в файл.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-108">The data from this array must be converted to Unicode because Visual Basic does not have a way to write bytes straight into a file.</span></span> <span data-ttu-id="a7d5d-109">Затем [**метод сетстреам**](record-setstream.md) может использовать файл преобразованных данных для записи потоковых данных в указанное поле записи [**объекта записи**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="a7d5d-109">The [**SetStream method**](record-setstream.md) can then use the file of converted data to write stream data into a specified record field of a [**Record object**](record-object.md).</span></span> <span data-ttu-id="a7d5d-110">Обратите внимание, что преобразование байтовых данных в Юникод может привести к изменению данных и того, что преобразованные данные должны соответствовать исходным данным для проверки правильности подписи.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-110">Note that conversion of the byte data to Unicode can potentially change the data and that the converted data must match the original data for correct signature verification.</span></span> <span data-ttu-id="a7d5d-111">Автор пакета должен убедиться, что исходные и преобразованные данные совпадают.</span><span class="sxs-lookup"><span data-stu-id="a7d5d-111">The package author must ensure that the original and converted data match.</span></span>


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



 

 
