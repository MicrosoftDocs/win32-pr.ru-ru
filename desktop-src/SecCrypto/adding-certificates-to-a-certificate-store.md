---
description: Сертификаты можно добавлять или удалять из хранилищ сертификатов, если хранилище открыто с разрешением на чтение и запись.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Добавление сертификатов в хранилище сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c4b2fafbcd11bf2d984dfd5b5a575f67dc4f6d3c70337de399ca6076029ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774039"
---
# <a name="adding-certificates-to-a-certificate-store"></a>Добавление сертификатов в хранилище сертификатов

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

[*Сертификаты*](../secgloss/c-gly.md) можно добавлять или удалять из [*хранилищ сертификатов*](../secgloss/c-gly.md) , если хранилище открыто с разрешением на чтение и запись. Разрешения на чтение и запись не предоставлены Active Directory хранилищам. Хотя сертификаты могут быть добавлены или удалены из хранилищ памяти, изменения в хранилищах памяти не сохраняются между сеансами.

Сертификаты можно добавить в хранилище сертификатов, открытое с разрешением на чтение и запись, с помощью метода **Add** . Сертификат можно удалить из хранилища сертификатов, открытого с разрешением на чтение и запись, с помощью метода **Remove** . Новые магазины можно создавать и сохранять в \_ расположениях "CAPICOM Current \_ User" и " \_ CAPICOM \_ Local \_ Machine Store" \_ . Вновь созданные хранилища в любом из этих расположений можно открыть с разрешением на чтение и запись.

В следующем примере открыто два хранилища сертификатов. Сертификаты субъектов с фамилиями, начинающимися с F, извлекаются из хранилища Active Directory. В этом случае хранилище CAPICOM \_ Current \_ User Store \_ , CAPICOM CA Store, \_ \_ открывается как хранилище для чтения и записи, а первый сертификат из коллекции сертификатов в хранилище Active Directory добавляется в сертификаты в \_ хранилище CAPICOM CA \_ .

В демонстрационных целях в примере показано открытие магазинов в расположениях "CAPICOM \_ Memory \_ Store", "CAPICOM \_ Current \_ user \_ Store" и "CAPICOM \_ Local \_ Machine Store" \_ . В примере показано, как экспортировать все сертификаты из открытого хранилища, записать экспортированные сертификаты в файл, прочитать их обратно и импортировать в другое хранилище. Вновь импортированные сертификаты будут перечислены и отображены.

При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** . Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md). Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.

В следующем примере показано открытие хранилищ сертификатов с помощью раннего связывания в объявлении объектов **хранилища** и при создании экземпляра этих объектов.


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
