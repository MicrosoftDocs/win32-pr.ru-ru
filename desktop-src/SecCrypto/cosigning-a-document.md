---
description: Документ может быть подписан более чем одним подписывающий.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Подписывание документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb384ef47001f1df85810ac37595988da96a356ff3b36b1b140d1a6f54d0d698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769389"
---
# <a name="cosigning-a-document"></a>Подписывание документа

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

Документ может быть подписан более чем одним подписывающий. Это происходит, если, например, две или более стороны подписывают контракт или отчет о расходах. В следующем примере документ, который уже подписан, получает второй подписывающий. Этот подписывающий использует метод [**подписывания**](signeddata-cosign.md) , чтобы присоединить дополнительную сигнатуру к документу.

При возникновении любой ошибки CAPICOM в свойстве **Err. Number** возвращается отрицательное значение. Дополнительные сведения о кодах ошибок CAPICOM см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md). если код ошибки в свойстве **Err. Number** имеет положительное значение, то ошибка является Windows ошибкой. дополнительные сведения о Windows кодах ошибок см. в файле Winerror. h.

> [!Note]
> При соподписании документа также требуется, чтобы у него был доступный [*сертификат*](../secgloss/c-gly.md) с [*закрытым ключом*](../secgloss/p-gly.md) для создания подписи. Если подписавший не указан в вызове метода [**Sign**](signeddata-sign.md) и в элементе CAPICOM \_ My Store нет сертификата \_ со связанным закрытым ключом, метод завершается ошибкой. Если в CAPICOM My Store есть один и только один \_ сертификат \_ со связанным закрытым ключом, используется этот ключ и сертификат. Если имеется более одного пригодного для использования сертификата, отображается запрос, позволяющий пользователю выбрать нужный сертификат.
> 
> Если метод [**подписывания**](signeddata-cosign.md) используется в веб-приложении, то перед созданием подписи с помощью закрытого ключа этого средства всегда отображается запрос на получение разрешения пользователя.

 

В следующем примере выполняется чтение файлов, содержащих документ, которые должны быть подписаны, и текущих подписей этого документа, подпись соподписана, а новая сигнатура записывается в файл. В примере используется отсоединенная подпись с подписанными данными и подписью в отдельных файлах.


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
