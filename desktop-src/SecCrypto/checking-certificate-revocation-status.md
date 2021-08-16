---
description: CAPICOM не включает проверку отзыва сертификатов по умолчанию.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Проверка состояния отзыва сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf1ce98e392da94fd800316fe63c5b79c8572a319c6db4246e7907eb80966d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769543"
---
# <a name="checking-certificate-revocation-status"></a>Проверка состояния отзыва сертификата

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

CAPICOM не включает проверку отзыва сертификатов по умолчанию. Однако проверку отзыва сертификатов можно включить программно для определенного сертификата с помощью свойства **IsValid. чеккфлаг** объекта Certificate. После установки соответствующего значения **чеккфлаг** доступ к свойству **IsValid** объекта сертификата или созданию пути проверки сертификата с помощью метода построения объекта цепочки приводит к проверке отзыва.

В следующем примере экземпляр CERT был создан как допустимый CAPICOM-сертификат.


```VB
Dim cert As Certificate
Dim LocalStore As New Store

' Open the My store.
LocalStore.Open LocalStore.Open CAPICOM_CURRENT_USER_STORE, _
    CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_WRITE

' Get the first certificate in the My store.
set cert = LocalStore.Certificates.Item(1)

cert.IsValid.CheckFlag = CAPICOM_CHECK_TRUSTED_ROOT Or _ 
   CAPICOM_CHECK_TIME_VALIDITY Or _ 
   CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
   CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
If cert.IsValid.Result Then
'CERTIFICATE IS VALID!
Else
Dim chain As New Chain
     chain.Build (cert)
     If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
     End If
     If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
'THE REVOCATION STATUS COULD NOT BE DETERMINED
     End If
End If

```



Предыдущее относится к отдельному сертификату независимо от того, как он был получен. Проверка отзыва сертификатов в объекте [**сигнеддата**](signeddata.md) не отличается, так как метод [**проверки**](signeddata-verify.md) объекта **сигнеддата** не может быть использован для этой цели, поскольку включение функции проверки \_ наличия \_ подписи и сертификата CAPICOM \_ не \_ приводит к проверке списка отзыва сертификатов.

Вместо этого для каждого сертификата подписи необходимо задать **чеккфлаг** . Рассмотрим следующий пример, где экземпляр sdata был создан как допустимый объект CAPICOM [**сигнеддата**](signeddata.md) .


```VB
Dim cert As Certificate
Dim chain As New Chain

' sData is an existing SignedData object.

For I = 1 To sData.Certificates.Count
   set cert = sData.Certificates(I) 
   cert.IsValid.CheckFlag = _ 
       CAPICOM_CHECK_TRUSTED_ROOT Or _ 
       CAPICOM_CHECK_TIME_VALIDITY Or _ 
       CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
       CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
   If cert.IsValid.Result Then
      'THE CERTIFICATE IS VALID!
   Else
      chain.Build cert
      If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
         'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
      End If
      If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
         'THE REVOCATION STATUS COULD NOT BE DETERMINED
      End If
   End If
Next I
```



Дополнительный пример — это цикл по всем сертификатам в объекте [**сигнеддата**](signeddata.md) .

 

 



