---
description: Указывает имя шаблона сертификата.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'Метод Искрденр:: Сетцерттемплатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683502"
---
# <a name="iscrdenrsetcerttemplatename-method"></a><span data-ttu-id="34e4a-103">Метод Искрденр:: Сетцерттемплатенаме</span><span class="sxs-lookup"><span data-stu-id="34e4a-103">ISCrdEnr::setCertTemplateName method</span></span>

<span data-ttu-id="34e4a-104">Метод **сетцерттемплатенаме** задает имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="34e4a-104">The **setCertTemplateName** method specifies the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e4a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34e4a-105">Syntax</span></span>


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="34e4a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34e4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e4a-107">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e4a-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e4a-108">Значение, которое определяет, устанавливается ли реальное имя или отображаемое имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="34e4a-108">Value which determines if the certificate template's real name or display name is being set.</span></span> <span data-ttu-id="34e4a-109">Если для *dwFlags* задано значение \_ \_ \_ \_ Отображаемое имя шаблона сертификата регистрации бросить, то \_ будет задано отображаемое имя шаблона сертификатов.</span><span class="sxs-lookup"><span data-stu-id="34e4a-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is set.</span></span> <span data-ttu-id="34e4a-110">В противном случае задается реальное имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="34e4a-110">Otherwise, the real name of the certificate template is set.</span></span>

</dd> <dt>

<span data-ttu-id="34e4a-111">*бстрцерттемплатенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e4a-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e4a-112">Имя шаблона сертификата, который будет использоваться в запросе сертификата.</span><span class="sxs-lookup"><span data-stu-id="34e4a-112">Name of the certificate template which will be used in the certificate request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e4a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34e4a-113">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="34e4a-114">VB</span><span class="sxs-lookup"><span data-stu-id="34e4a-114">VB</span></span>

<span data-ttu-id="34e4a-115">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="34e4a-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="34e4a-116">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="34e4a-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="34e4a-117">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="34e4a-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34e4a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34e4a-118">Remarks</span></span>

<span data-ttu-id="34e4a-119">Если имя шаблона сертификата не задано путем вызова **искрденр:: сетцерттемплатенаме**, по умолчанию используется имя в списке доступных шаблонов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="34e4a-119">If you do not set the certificate template name by calling **ISCrdEnr::setCertTemplateName**, the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e4a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="34e4a-120">Requirements</span></span>



| <span data-ttu-id="34e4a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="34e4a-121">Requirement</span></span> | <span data-ttu-id="34e4a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="34e4a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34e4a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34e4a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="34e4a-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="34e4a-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="34e4a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34e4a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="34e4a-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34e4a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34e4a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="34e4a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34e4a-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34e4a-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="34e4a-129">IID</span><span class="sxs-lookup"><span data-stu-id="34e4a-129">IID</span></span><br/>                      | <span data-ttu-id="34e4a-130">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="34e4a-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="34e4a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34e4a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e4a-132">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="34e4a-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="34e4a-133">**Искрденр:: Жетцерттемплатенаме**</span><span class="sxs-lookup"><span data-stu-id="34e4a-133">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




