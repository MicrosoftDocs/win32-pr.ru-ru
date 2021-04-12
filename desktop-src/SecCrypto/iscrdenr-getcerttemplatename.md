---
description: Извлекает имя шаблона сертификата.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'Метод Искрденр:: Жетцерттемплатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272259"
---
# <a name="iscrdenrgetcerttemplatename-method"></a><span data-ttu-id="0aa65-103">Метод Искрденр:: Жетцерттемплатенаме</span><span class="sxs-lookup"><span data-stu-id="0aa65-103">ISCrdEnr::getCertTemplateName method</span></span>

<span data-ttu-id="0aa65-104">Метод **жетцерттемплатенаме** извлекает имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="0aa65-104">The **getCertTemplateName** method retrieves the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0aa65-105">Syntax</span></span>


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="0aa65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0aa65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa65-107">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0aa65-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa65-108">Значение, определяющее, возвращается ли вещественное имя или отображаемое имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="0aa65-108">A value that determines whether the certificate template's real name or display name is returned.</span></span> <span data-ttu-id="0aa65-109">Если для *dwFlags* задано значение \_ \_ \_ \_ Отображаемое имя шаблона сертификата регистрации, то выводится \_ Отображаемое имя шаблона сертификатов. в противном случае отображается действительное имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="0aa65-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is retrieved; otherwise, the real name of the certificate template is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="0aa65-110">*пбстрцерттемплатенаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0aa65-110">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa65-111">Указатель на строку, которая возвращает имя шаблона сертификата, который будет использоваться в [*запросе сертификата*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0aa65-111">A pointer to a string that returns the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa65-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aa65-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="0aa65-113">C++</span><span class="sxs-lookup"><span data-stu-id="0aa65-113">C++</span></span>

<span data-ttu-id="0aa65-114">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0aa65-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="0aa65-115">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="0aa65-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="0aa65-116">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="0aa65-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="0aa65-117">VB</span><span class="sxs-lookup"><span data-stu-id="0aa65-117">VB</span></span>

<span data-ttu-id="0aa65-118">Строка, представляющая имя шаблона сертификата, который будет использоваться в [*запросе сертификата*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0aa65-118">A string that represents the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa65-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0aa65-119">Remarks</span></span>

<span data-ttu-id="0aa65-120">Если имя шаблона сертификата не задано путем вызова [**искрденр:: сетцерттемплатенаме**](iscrdenr-setcerttemplatename.md), по умолчанию используется имя в списке доступных шаблонов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0aa65-120">If you do not set the certificate template name by calling [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa65-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0aa65-121">Requirements</span></span>



| <span data-ttu-id="0aa65-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0aa65-122">Requirement</span></span> | <span data-ttu-id="0aa65-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0aa65-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa65-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0aa65-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa65-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0aa65-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0aa65-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0aa65-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa65-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0aa65-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0aa65-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0aa65-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aa65-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aa65-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="0aa65-130">IID</span><span class="sxs-lookup"><span data-stu-id="0aa65-130">IID</span></span><br/>                      | <span data-ttu-id="0aa65-131">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="0aa65-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="0aa65-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0aa65-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa65-133">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="0aa65-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="0aa65-134">**Искрденр:: Сетцерттемплатенаме**</span><span class="sxs-lookup"><span data-stu-id="0aa65-134">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
