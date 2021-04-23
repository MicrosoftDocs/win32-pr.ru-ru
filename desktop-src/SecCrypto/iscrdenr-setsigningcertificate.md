---
description: Указывает сертификат для подписи (также известный как сертификат агента регистрации).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'Метод Искрденр:: Сетсигнингцертификате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664630"
---
# <a name="iscrdenrsetsigningcertificate-method"></a><span data-ttu-id="d4d39-103">Метод Искрденр:: Сетсигнингцертификате</span><span class="sxs-lookup"><span data-stu-id="d4d39-103">ISCrdEnr::setSigningCertificate method</span></span>

<span data-ttu-id="d4d39-104">Метод **сетсигнингцертификате** указывает сертификат подписи (также известный как *сертификат агента регистрации*).</span><span class="sxs-lookup"><span data-stu-id="d4d39-104">The **setSigningCertificate** method specifies a signing certificate (also known as the *enrollment agent certificate*).</span></span>

<span data-ttu-id="d4d39-105">Перед регистрацией от имени пользователей необходимо выбрать или задать сертификат для подписи.</span><span class="sxs-lookup"><span data-stu-id="d4d39-105">Before enrolling on behalf of users, you must select or set a signing certificate.</span></span> <span data-ttu-id="d4d39-106">[*Закрытый ключ*](../secgloss/p-gly.md) , связанный с этим сертификатом подписи, используется для подписания \# запроса PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="d4d39-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="d4d39-107">\#В свою очередь, PKCS 7 содержит \# запрос PKCS 10 пользователя (который подписан с помощью закрытого ключа пользователя).</span><span class="sxs-lookup"><span data-stu-id="d4d39-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d39-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4d39-108">Syntax</span></span>


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="d4d39-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4d39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d39-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4d39-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d39-111">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="d4d39-111">Reserved for future use.</span></span> <span data-ttu-id="d4d39-112">Присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="d4d39-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="d4d39-113">*бстрцерттемплатенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4d39-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d39-114">Имя шаблона сертификата для сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="d4d39-114">Name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="d4d39-115">Если вы получили сертификат Енроллментажент, можно использовать значение "Енроллментажент".</span><span class="sxs-lookup"><span data-stu-id="d4d39-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d39-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4d39-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="d4d39-117">VB</span><span class="sxs-lookup"><span data-stu-id="d4d39-117">VB</span></span>

<span data-ttu-id="d4d39-118">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d4d39-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="d4d39-119">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="d4d39-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="d4d39-120">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="d4d39-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d39-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4d39-121">Remarks</span></span>

<span data-ttu-id="d4d39-122">Перед регистрацией от имени пользователя сначала необходимо получить сертификат подписи.</span><span class="sxs-lookup"><span data-stu-id="d4d39-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="d4d39-123">Сертификат для подписи можно получить с помощью оснастки MMC диспетчера сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d4d39-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="d4d39-124">Метод **сетсигнингцертификате** не получает сертификат для подписи, но информирует Управление регистрацией смарт-карты, которое ранее получило сертификат подписи для использования.</span><span class="sxs-lookup"><span data-stu-id="d4d39-124">The **setSigningCertificate** method does not obtain the signing certificate but informs the Smart Card Enrollment Control which previously obtained signing certificate to use.</span></span> <span data-ttu-id="d4d39-125">Метод **сетсигнингцертификате** выполняет поиск последнего сертификата подписи в хранилище "My" вызывающего объекта, соответствующего шаблону сертификата, заданному параметром *бстрцерттемплатенаме*.</span><span class="sxs-lookup"><span data-stu-id="d4d39-125">The **setSigningCertificate** method searches the caller's "My" store for the most recent signing certificate corresponding to the certificate template specified by *bstrCertTemplateName*.</span></span>

<span data-ttu-id="d4d39-126">Альтернативой для **сетсигнингцертификате** является **Искрденр:: сетсигнингцертификате**.</span><span class="sxs-lookup"><span data-stu-id="d4d39-126">An alternative to **setSigningCertificate** is **ISCrdEnr::setSigningCertificate**.</span></span>

<span data-ttu-id="d4d39-127">После установки сертификата для подписи его имя можно получить, вызвав [**искрденр:: жетсигнингцертификатенаме**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="d4d39-127">After a signing certificate is set, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d39-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d4d39-128">Requirements</span></span>



| <span data-ttu-id="d4d39-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d4d39-129">Requirement</span></span> | <span data-ttu-id="d4d39-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d4d39-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d39-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4d39-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d39-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4d39-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d4d39-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4d39-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d39-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4d39-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4d39-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d4d39-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4d39-136"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4d39-136"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4d39-137">IID</span><span class="sxs-lookup"><span data-stu-id="d4d39-137">IID</span></span><br/>                      | <span data-ttu-id="d4d39-138">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="d4d39-138">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d4d39-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4d39-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d39-140">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="d4d39-140">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="d4d39-141">**Искрденр:: Жетсигнингцертификатенаме**</span><span class="sxs-lookup"><span data-stu-id="d4d39-141">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
