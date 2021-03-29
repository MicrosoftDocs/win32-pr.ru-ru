---
description: Используется для определения того, содержит ли шаблон сертификата \_ \_ \_ Использование ключа защиты электронной почты сзоид пкикс \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'Метод Искрденр:: Жетцерттемплатесмиме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912016"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a><span data-ttu-id="4f480-103">Метод Искрденр:: Жетцерттемплатесмиме</span><span class="sxs-lookup"><span data-stu-id="4f480-103">ISCrdEnr::getCertTemplateSMIME method</span></span>

<span data-ttu-id="4f480-104">Метод **жетцерттемплатесмиме** используется для определения того, содержит ли шаблон сертификата \_ \_ \_ Использование ключа защиты электронной почты сзоид пкикс \_ .</span><span class="sxs-lookup"><span data-stu-id="4f480-104">The **getCertTemplateSMIME** method is used to determine whether a certificate template contains the szOID\_PKIX\_KP\_EMAIL\_PROTECTION key usage.</span></span>

<span data-ttu-id="4f480-105">Если это использование ключа является частью шаблона сертификата, шаблон сертификата поддерживает операции с [*безопасными и многоцелевыми расширениями электронной почты Интернета*](../secgloss/s-gly.md) (S/MIME).</span><span class="sxs-lookup"><span data-stu-id="4f480-105">If this key usage is part of the certificate template, the certificate template supports [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f480-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f480-106">Syntax</span></span>


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a><span data-ttu-id="4f480-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f480-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f480-108">*бстрцерттемплатенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f480-108">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f480-109">Имя сертификата, для которого запрашивается использование ключа S/MIME.</span><span class="sxs-lookup"><span data-stu-id="4f480-109">The name of the certificate being queried for the S/MIME key usage.</span></span>

</dd> <dt>

<span data-ttu-id="4f480-110">*пдвцерттемплатесмиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4f480-110">*pdwCertTemplateSMIME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f480-111">Указатель на **DWORD** , возвращающий значение, равное 1, если *бстрцерттемплатенаме* поддерживает S/MIME; в противном случае возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="4f480-111">A pointer to a **DWORD** that returns a value of one if *bstrCertTemplateName* supports S/MIME; otherwise it returns zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f480-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f480-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="4f480-113">C++</span><span class="sxs-lookup"><span data-stu-id="4f480-113">C++</span></span>

<span data-ttu-id="4f480-114">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4f480-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="4f480-115">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="4f480-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4f480-116">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="4f480-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="4f480-117">VB</span><span class="sxs-lookup"><span data-stu-id="4f480-117">VB</span></span>

<span data-ttu-id="4f480-118">Значение **типа Long** , равное единице, если *бстрцерттемплатенаме* поддерживает S/MIME; в противном случае — ноль.</span><span class="sxs-lookup"><span data-stu-id="4f480-118">**Long** value of one if *bstrCertTemplateName* supports S/MIME; otherwise zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f480-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f480-119">Remarks</span></span>

<span data-ttu-id="4f480-120">Константа для \_ \_ защиты электронной почты сзоид пкикс-ключевого средства \_ \_ определяется в винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="4f480-120">The constant for szOID\_PKIX\_KP\_EMAIL\_PROTECTION is defined in Wincrypt.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f480-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4f480-121">Requirements</span></span>



| <span data-ttu-id="4f480-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4f480-122">Requirement</span></span> | <span data-ttu-id="4f480-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4f480-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f480-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f480-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4f480-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4f480-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4f480-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f480-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4f480-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f480-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f480-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4f480-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f480-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f480-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f480-130">IID</span><span class="sxs-lookup"><span data-stu-id="4f480-130">IID</span></span><br/>                      | <span data-ttu-id="4f480-131">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="4f480-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="4f480-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f480-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f480-133">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="4f480-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="4f480-134">[**Искрденр:: регистрация**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f480-134">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
