---
description: Извлекает имя субъекта из сертификата подписи.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'Метод Искрденр:: Жетсигнингцертификатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423961"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a><span data-ttu-id="719c4-103">Метод Искрденр:: Жетсигнингцертификатенаме</span><span class="sxs-lookup"><span data-stu-id="719c4-103">ISCrdEnr::getSigningCertificateName method</span></span>

<span data-ttu-id="719c4-104">Метод **жетсигнингцертификатенаме** извлекает имя субъекта из сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="719c4-104">The **getSigningCertificateName** method retrieves the subject name from the signing certificate.</span></span>

<span data-ttu-id="719c4-105">Этот метод также можно использовать для вывода сертификата в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="719c4-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="719c4-106">Этот метод вызывает функцию [*CryptoAPI*](../secgloss/c-gly.md) [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="719c4-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="719c4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="719c4-107">Syntax</span></span>


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="719c4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="719c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="719c4-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="719c4-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719c4-110">Значение, определяющее, отображается ли сертификат в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="719c4-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="719c4-111">Если это значение равно бросить \_ Регистрация \_ не \_ отображает сертификат \_ (определенный как 0x01), сертификат подписи не отображается; любые другие значения приводят к тому, что сертификат подписи отображается в диалоговом окне **сертификат** .</span><span class="sxs-lookup"><span data-stu-id="719c4-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the signing certificate is not displayed; any other values result in the signing certificate being displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="719c4-112">*пбстрсигнингцертнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="719c4-112">*pbstrSigningCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="719c4-113">Указатель на строку, которая возвращает имя сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="719c4-113">A pointer to a string that returns the name of the signing certificate.</span></span> <span data-ttu-id="719c4-114">Сертификат для подписи будет использоваться для подписания [*запроса на сертификат*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="719c4-114">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="719c4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="719c4-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="719c4-116">C++</span><span class="sxs-lookup"><span data-stu-id="719c4-116">C++</span></span>

<span data-ttu-id="719c4-117">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="719c4-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="719c4-118">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="719c4-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="719c4-119">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="719c4-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="719c4-120">VB</span><span class="sxs-lookup"><span data-stu-id="719c4-120">VB</span></span>

<span data-ttu-id="719c4-121">Строка, представляющая имя сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="719c4-121">A string that represents the name of the signing certificate.</span></span> <span data-ttu-id="719c4-122">Сертификат для подписи будет использоваться для подписания [*запроса на сертификат*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="719c4-122">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="719c4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="719c4-123">Remarks</span></span>

<span data-ttu-id="719c4-124">Метод **жетсигнингцертификатенаме** возвращает имя субъекта сертификата, выбранного вами (или другим администратором) в предыдущем успешном вызове [**Искрденр:: селектсигнингцертификате**](iscrdenr-selectsigningcertificate.md) или [**искрденр:: сетсигнингцертификате**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="719c4-124">The **getSigningCertificateName** method returns the subject name of the certificate you (or another administrator) have selected in a previous successful call to [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) or [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span> <span data-ttu-id="719c4-125">Этот метод вызывает функцию [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) для получения имени субъекта в соответствии с последовательностью, описанной \_ для \_ \_ значения простого отображаемого типа сертификата для \_ параметра *двтипе* **цертжетнаместринг**.</span><span class="sxs-lookup"><span data-stu-id="719c4-125">This method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the subject name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="719c4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="719c4-126">Requirements</span></span>



| <span data-ttu-id="719c4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="719c4-127">Requirement</span></span> | <span data-ttu-id="719c4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="719c4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="719c4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="719c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="719c4-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="719c4-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="719c4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="719c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="719c4-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="719c4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="719c4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="719c4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="719c4-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="719c4-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="719c4-135">IID</span><span class="sxs-lookup"><span data-stu-id="719c4-135">IID</span></span><br/>                      | <span data-ttu-id="719c4-136">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="719c4-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="719c4-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="719c4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="719c4-138">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="719c4-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="719c4-139">**Искрденр:: Селектсигнингцертификате**</span><span class="sxs-lookup"><span data-stu-id="719c4-139">**ISCrdEnr::selectSigningCertificate**</span></span>](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
