---
description: CAPICOM не включает проверку отзыва сертификатов по умолчанию.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Проверка состояния отзыва сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada134bbca88b1a875ff27add7566116cf7334bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265770"
---
# <a name="checking-certificate-revocation-status"></a><span data-ttu-id="2c8fb-103">Проверка состояния отзыва сертификата</span><span class="sxs-lookup"><span data-stu-id="2c8fb-103">Checking Certificate Revocation Status</span></span>

<span data-ttu-id="2c8fb-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2c8fb-105">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="2c8fb-106">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="2c8fb-107">CAPICOM не включает проверку отзыва сертификатов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-107">CAPICOM does not enable certificate revocation checking by default.</span></span> <span data-ttu-id="2c8fb-108">Однако проверку отзыва сертификатов можно включить программно для определенного сертификата с помощью свойства **IsValid. чеккфлаг** объекта Certificate.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-108">However, certificate revocation checking can be enabled programmatically for a particular certificate through the **IsValid.CheckFlag** property of a Certificate object.</span></span> <span data-ttu-id="2c8fb-109">После установки соответствующего значения **чеккфлаг** доступ к свойству **IsValid** объекта сертификата или созданию пути проверки сертификата с помощью метода построения объекта цепочки приводит к проверке отзыва.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-109">After the appropriate value of **CheckFlag** has been set, accessing the Certificate object's **IsValid.Result** property or building the certificate's verification path using a Chain object's Build method forces revocation checking.</span></span>

<span data-ttu-id="2c8fb-110">В следующем примере экземпляр CERT был создан как допустимый CAPICOM-сертификат.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-110">In the following example, cert has been instantiated as a valid CAPICOM certificate.</span></span>


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



<span data-ttu-id="2c8fb-111">Предыдущее относится к отдельному сертификату независимо от того, как он был получен.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-111">The preceding applies to an individual certificate, no matter how it was obtained.</span></span> <span data-ttu-id="2c8fb-112">Проверка отзыва сертификатов в объекте [**сигнеддата**](signeddata.md) не отличается, так как метод [**проверки**](signeddata-verify.md) объекта **сигнеддата** не может быть использован для этой цели, поскольку включение функции проверки \_ наличия \_ подписи и сертификата CAPICOM \_ не \_ приводит к проверке списка отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-112">Performing revocation checking on the certificates in a [**SignedData**](signeddata.md) object is no different because the **SignedData** object's [**Verify**](signeddata-verify.md) method cannot be used for this purpose because enabling CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE does not cause CRL checking.</span></span>

<span data-ttu-id="2c8fb-113">Вместо этого для каждого сертификата подписи необходимо задать **чеккфлаг** .</span><span class="sxs-lookup"><span data-stu-id="2c8fb-113">Instead, the **CheckFlag** must be set for each signer's certificate.</span></span> <span data-ttu-id="2c8fb-114">Рассмотрим следующий пример, где экземпляр sdata был создан как допустимый объект CAPICOM [**сигнеддата**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="2c8fb-114">Consider the following example where sData has been instantiated as a valid CAPICOM [**SignedData**](signeddata.md) object.</span></span>


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



<span data-ttu-id="2c8fb-115">Дополнительный пример — это цикл по всем сертификатам в объекте [**сигнеддата**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="2c8fb-115">The additional example is the loop over all the certificates in the [**SignedData**](signeddata.md) object.</span></span>

 

 



