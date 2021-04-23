---
description: Извлекает количество шаблонов сертификатов.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'Метод Искрденр:: Жетцерттемплатекаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912827"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a><span data-ttu-id="9465c-103">Метод Искрденр:: Жетцерттемплатекаунт</span><span class="sxs-lookup"><span data-stu-id="9465c-103">ISCrdEnr::getCertTemplateCount method</span></span>

<span data-ttu-id="9465c-104">Метод **жетцерттемплатекаунт** извлекает количество шаблонов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9465c-104">The **getCertTemplateCount** method retrieves the number of certificate templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9465c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9465c-105">Syntax</span></span>


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a><span data-ttu-id="9465c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9465c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9465c-107">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9465c-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9465c-108">Значение, определяющее, предназначен ли шаблон для сертификатов пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="9465c-108">A value that determines whether the template is for user or machine certificates.</span></span> <span data-ttu-id="9465c-109">Если это значение равно бросить \_ зарегистрировать \_ \_ шаблон сертификата пользователя \_ (определяется как 1), то возвращаемое количество будет использоваться для шаблонов сертификатов пользователей.</span><span class="sxs-lookup"><span data-stu-id="9465c-109">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1) then the returned count will be for user certificate templates.</span></span> <span data-ttu-id="9465c-110">Если это значение равно бросить \_ зарегистрировать \_ \_ шаблон сертификата компьютера \_ (определяется как 2), то возвращаемое количество будет использоваться для шаблонов сертификатов компьютера.</span><span class="sxs-lookup"><span data-stu-id="9465c-110">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2) then the returned count will be for machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="9465c-111">*пдвцерттемплатекаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9465c-111">*pdwCertTemplateCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9465c-112">Указатель на значение **типа Long** , возвращающее число шаблонов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9465c-112">A pointer to a **LONG** that returns the number of certificate templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9465c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9465c-113">Return value</span></span>

### <a name="c"></a><span data-ttu-id="9465c-114">C++</span><span class="sxs-lookup"><span data-stu-id="9465c-114">C++</span></span>

<span data-ttu-id="9465c-115">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9465c-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="9465c-116">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="9465c-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="9465c-117">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="9465c-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="9465c-118">VB</span><span class="sxs-lookup"><span data-stu-id="9465c-118">VB</span></span>

<span data-ttu-id="9465c-119">Значение **типа Long** , представляющее количество шаблонов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9465c-119">A **Long** value that represents the number of certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="9465c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9465c-120">Requirements</span></span>



| <span data-ttu-id="9465c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9465c-121">Requirement</span></span> | <span data-ttu-id="9465c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9465c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9465c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9465c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9465c-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9465c-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9465c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9465c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9465c-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9465c-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9465c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9465c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9465c-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9465c-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="9465c-129">IID</span><span class="sxs-lookup"><span data-stu-id="9465c-129">IID</span></span><br/>                      | <span data-ttu-id="9465c-130">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="9465c-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="9465c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9465c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9465c-132">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="9465c-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="9465c-133">**Искрденр:: Енумцерттемплатенаме**</span><span class="sxs-lookup"><span data-stu-id="9465c-133">**ISCrdEnr::enumCertTemplateName**</span></span>](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




