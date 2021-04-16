---
description: 'Возвращает имя сертификата, полученное в результате предыдущего успешного вызова Искрденр:: RECALL.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'Метод Искрденр:: Жетенролледцертификатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684095"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a><span data-ttu-id="7a832-103">Метод Искрденр:: Жетенролледцертификатенаме</span><span class="sxs-lookup"><span data-stu-id="7a832-103">ISCrdEnr::getEnrolledCertificateName method</span></span>

<span data-ttu-id="7a832-104">Метод **жетенролледцертификатенаме** извлекает имя сертификата, полученного при предыдущем успешном вызове [**искрденр::**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))Recall.</span><span class="sxs-lookup"><span data-stu-id="7a832-104">The **getEnrolledCertificateName** method retrieves the name of the certificate resulting from an earlier successful call to [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span></span>

<span data-ttu-id="7a832-105">Этот метод также можно использовать для вывода сертификата в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="7a832-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="7a832-106">Этот метод вызывает функцию [*CryptoAPI*](../secgloss/c-gly.md) [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="7a832-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a832-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a832-107">Syntax</span></span>


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="7a832-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a832-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a832-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a832-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a832-110">Значение, определяющее, отображается ли сертификат в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="7a832-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="7a832-111">Если это значение равно бросить \_ Регистрация \_ не \_ отображает \_ сертификат (определенный как 0x01), зарегистрированный сертификат не отображается; любые другие значения приводят к отображению зарегистрированного сертификата в диалоговом окне **сертификат** .</span><span class="sxs-lookup"><span data-stu-id="7a832-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the enrolled certificate is not displayed; any other values cause the enrolled certificate to be displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="7a832-112">*пбстрцертнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7a832-112">*pBstrCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a832-113">Указатель на строку, которая возвращает полученное имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="7a832-113">A pointer to a string that returns the retrieved certificate name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a832-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a832-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="7a832-115">C++</span><span class="sxs-lookup"><span data-stu-id="7a832-115">C++</span></span>

<span data-ttu-id="7a832-116">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7a832-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="7a832-117">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="7a832-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="7a832-118">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="7a832-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="7a832-119">VB</span><span class="sxs-lookup"><span data-stu-id="7a832-119">VB</span></span>

<span data-ttu-id="7a832-120">Строка, представляющая полученное имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="7a832-120">A string that represents the retrieved certificate name.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a832-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a832-121">Remarks</span></span>

<span data-ttu-id="7a832-122">Так как этот метод работает с существующим сертификатом, необходимо успешно вызвать [**искрденр::**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) Call, прежде чем можно будет вызвать **жетенролледцертификатенаме**.</span><span class="sxs-lookup"><span data-stu-id="7a832-122">Because this method operates on an existing certificate, you must have successfully called [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) before you can call **getEnrolledCertificateName**.</span></span>

<span data-ttu-id="7a832-123">Метод **жетенролледцертификатенаме** вызывает функцию [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) для получения имени сертификата в соответствии с последовательностью, описанной для \_ \_ \_ значения простого отображаемого типа сертификата для \_ параметра **цертжетнаместринг** *двтипе* .</span><span class="sxs-lookup"><span data-stu-id="7a832-123">The **getEnrolledCertificateName** method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the certificate name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a832-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7a832-124">Requirements</span></span>



| <span data-ttu-id="7a832-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7a832-125">Requirement</span></span> | <span data-ttu-id="7a832-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7a832-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a832-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a832-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7a832-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7a832-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7a832-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a832-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7a832-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a832-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a832-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7a832-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a832-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a832-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a832-133">IID</span><span class="sxs-lookup"><span data-stu-id="7a832-133">IID</span></span><br/>                      | <span data-ttu-id="7a832-134">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="7a832-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="7a832-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a832-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a832-136">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="7a832-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="7a832-137">[**Искрденр:: регистрация**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7a832-137">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
