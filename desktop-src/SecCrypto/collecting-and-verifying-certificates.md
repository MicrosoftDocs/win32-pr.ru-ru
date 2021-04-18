---
description: В следующем примере сертификаты в локальном хранилище перечисляются и проверяются на допустимость.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Сбор и проверка сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0b160f373d5ade65679fcc4dd87e3c1c86dc4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683162"
---
# <a name="collecting-and-verifying-certificates"></a>Сбор и проверка сертификатов

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

Часто требуется собрать и проверить группу [*сертификатов*](../secgloss/c-gly.md) . Это часто делается для подготовки группы получателей сообщения с оболочкой. В следующем примере сертификаты в локальном хранилище перечисляются и проверяются на допустимость. Далее открывается хранилище Active Directory для получения и добавления в локальное хранилище новых сертификатов. Сертификаты, полученные из хранилища Active Directory, проверяются на допустимость и, если они действительны, добавляются в локальное хранилище. Затем оба хранилища закрываются.

При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** . Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md). Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.

В этом примере имя локального хранилища передается в качестве строкового параметра. Строка, указывающая условия поиска для сертификатов в хранилище Active Directory, также передается в качестве параметра.


```VB
Sub CollectValidCerts(ByVal storename As String, ByVal _
    certname As String)

    On Error GoTo errorhandler

    ' Prepare a local certificate store to contain valid
    ' certificates for the recipients of an enveloped
    ' message.

    ' Open the local store and go to the certificates in the store
    '   1. Display the certificate
    '   2. Check the validity of the certificate
    '   3. Remove certificates that are not valid from the store

    Dim LocalStore As New Store
    Dim ADStore As New Store
    Dim i As Long

    LocalStore.Open(CAPICOM_CURRENT_USER_STORE, storename, _
        CAPICOM_STORE_OPEN_READ_WRITE)

    MsgBox("There are " & LocalStore.Certificates.Count & _
        " certificates in this store ")
    For i = 1 To LocalStore.Certificates.Count
        If LocalStore.Certificates.Item(i).IsValid Then
            LocalStore.Certificates.Item(i).Display()
        Else
            MsgBox("A certificate that is not valid was found.")
        End If
    Next i

    ' Open the AD store and retrieve a certificate based
    ' on a string passed into the function. Add any valid
    ' certificates found to the local store.

    ADStore.Open(CAPICOM_ACTIVE_DIRECTORY_USER_STORE, certname, _
        CAPICOM_STORE_OPEN_READ_ONLY)
    MsgBox("There are " & ADStore.Certificates.Count & _
        " certificates in the AD store.")

    For i = 1 To ADStore.Certificates.Count
        If ADStore.Certificates.Item(i).IsValid Then
            ADStore.Certificates.Item(i).Display()
            LocalStore.Add(ADStore.Certificates.Item(i))
        Else
            MsgBox("the certificate from the AD store is not valid.")
        End If
    Next i

    LocalStore = Nothing
    ADStore = Nothing
    MsgBox("Sub finished without error ")
    Exit Sub
errorhandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
