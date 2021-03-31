---
description: Отображает диалоговое окно Выбор сертификата, позволяющее выбрать сертификат подписи (также называемый сертификатом агента регистрации).
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'Метод Искрденр:: Селектсигнингцертификате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912824"
---
# <a name="iscrdenrselectsigningcertificate-method"></a><span data-ttu-id="7ec79-103">Метод Искрденр:: Селектсигнингцертификате</span><span class="sxs-lookup"><span data-stu-id="7ec79-103">ISCrdEnr::selectSigningCertificate method</span></span>

<span data-ttu-id="7ec79-104">Метод **селектсигнингцертификате** отображает диалоговое окно **Выбор сертификата** , позволяющее выбрать сертификат подписи (также называемый *сертификатом агента регистрации*).</span><span class="sxs-lookup"><span data-stu-id="7ec79-104">The **selectSigningCertificate** method displays a **Select Certificate** dialog box, allowing a signing certificate (also known as the *enrollment agent certificate*) to be selected.</span></span>

<span data-ttu-id="7ec79-105">Перед регистрацией от имени пользователей необходимо выбрать сертификат для подписи.</span><span class="sxs-lookup"><span data-stu-id="7ec79-105">Before enrolling on behalf of users, you must select a signing certificate.</span></span> <span data-ttu-id="7ec79-106">[*Закрытый ключ*](../secgloss/p-gly.md) , связанный с этим сертификатом подписи, используется для подписания \# запроса PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="7ec79-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="7ec79-107">\#В свою очередь, PKCS 7 содержит \# запрос PKCS 10 пользователя (который подписан с помощью закрытого ключа пользователя).</span><span class="sxs-lookup"><span data-stu-id="7ec79-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec79-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ec79-108">Syntax</span></span>


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="7ec79-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ec79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec79-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ec79-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec79-111">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7ec79-111">Reserved for future use.</span></span> <span data-ttu-id="7ec79-112">Присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="7ec79-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7ec79-113">*бстрцерттемплатенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ec79-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec79-114">Строка, представляющая имя шаблона сертификата для сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="7ec79-114">A string that represents the name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="7ec79-115">Если вы получили сертификат Енроллментажент, можно использовать значение "Енроллментажент".</span><span class="sxs-lookup"><span data-stu-id="7ec79-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec79-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ec79-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="7ec79-117">VB</span><span class="sxs-lookup"><span data-stu-id="7ec79-117">VB</span></span>

<span data-ttu-id="7ec79-118">Если метод завершается успешно, метод возвращает значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7ec79-118">If the method succeeds, the method returns **S\_OK**.</span></span>

<span data-ttu-id="7ec79-119">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="7ec79-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="7ec79-120">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="7ec79-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec79-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ec79-121">Remarks</span></span>

<span data-ttu-id="7ec79-122">Перед регистрацией от имени пользователя сначала необходимо получить сертификат подписи.</span><span class="sxs-lookup"><span data-stu-id="7ec79-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="7ec79-123">Сертификат для подписи можно получить с помощью оснастки MMC диспетчера сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7ec79-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="7ec79-124">Метод **селектсигнингцертификате** не получает сертификат подписи, но отображает диалоговое окно ранее полученных сертификатов для подписи, позволяя выбрать сертификат, который будет использоваться для подписания запросов регистрации от имени.</span><span class="sxs-lookup"><span data-stu-id="7ec79-124">The **selectSigningCertificate** method does not obtain the signing certificate but displays a dialog box of previously obtained signing certificates, allowing you to choose which certificate will be used to sign the enroll-on-behalf requests.</span></span>

<span data-ttu-id="7ec79-125">Альтернативой для **селектсигнингцертификате** является [**Искрденр:: сетсигнингцертификате**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="7ec79-125">An alternative to **selectSigningCertificate** is [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span>

<span data-ttu-id="7ec79-126">После выбора сертификата для подписи его имя можно получить, вызвав [**искрденр:: жетсигнингцертификатенаме**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="7ec79-126">After a signing certificate is selected, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec79-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7ec79-127">Requirements</span></span>



| <span data-ttu-id="7ec79-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7ec79-128">Requirement</span></span> | <span data-ttu-id="7ec79-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7ec79-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec79-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ec79-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec79-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7ec79-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7ec79-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ec79-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec79-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ec79-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ec79-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7ec79-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ec79-135"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ec79-135"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ec79-136">IID</span><span class="sxs-lookup"><span data-stu-id="7ec79-136">IID</span></span><br/>                      | <span data-ttu-id="7ec79-137">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="7ec79-137">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="7ec79-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ec79-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec79-139">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="7ec79-139">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="7ec79-140">**Искрденр:: Жетсигнингцертификатенаме**</span><span class="sxs-lookup"><span data-stu-id="7ec79-140">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
