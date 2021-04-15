---
description: Подпись обычно используется для подписи текста и сохранения этого подписанного текста в файл. Подписанный текст также может быть отправлен через Интернет. Подписанное сообщение находится в \# формате PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Подписание документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662116"
---
# <a name="signing-a-document"></a>Подписание документа

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

Подпись обычно используется для подписи текста и сохранения этого подписанного текста в файл. Подписанный текст также может быть отправлен через Интернет. Подписанное сообщение находится в \# формате PKCS 7.

В этом примере подпись создается для отсоединенного содержимого (если содержимое не включено в подпись). Отсоединенная сигнатура чаще всего используется, если получатель подписи имеет копию точного подписанного текста. В приведенном ниже примере исходное сообщение и отсоединенная подпись записываются в отдельные файлы.

При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** . Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md). Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.

При создании подписи используется [*закрытый ключ*](../secgloss/p-gly.md)подписывающий. Подпись можно создать, только если доступен сертификат подписавший с соответствующим закрытым ключом. В этом примере метода **Sign** не указан подписывающий. Если подписавший не указан и ни один из сертификатов в элементе **CAPICOM \_ My \_ Store** не имеет связанного закрытого ключа, то метод **Sign** завершается ошибкой. Если один и только один сертификат в элементе **CAPICOM \_ My \_ Store** имеет связанный закрытый ключ, то для создания подписи используется этот сертификат и его закрытый ключ. Если несколько сертификатов в хранилище **CAPICOM \_ My \_ Store** имеют связанный закрытый ключ, появляется диалоговое окно, и пользователь может выбрать сертификат, который будет использоваться для создания подписи.

Когда веб-приложение использует метод **Sign** , всегда отображается запрос, а перед подписью, использующей закрытый ключ этого пользователя, требуется разрешение.


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> <dt>

[**Подписавший. сертификат**](signer-certificate.md)
</dt> <dt>

[**attribute**](attribute.md)
</dt> <dt>

[**сигнеддата**](signeddata.md)
</dt> </dl>

 

 
