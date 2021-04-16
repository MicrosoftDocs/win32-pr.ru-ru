---
description: Перечисляет имена шаблонов сертификатов.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'Метод Искрденр:: Енумцерттемплатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664400"
---
# <a name="iscrdenrenumcerttemplatename-method"></a><span data-ttu-id="8cfd2-103">Метод Искрденр:: Енумцерттемплатенаме</span><span class="sxs-lookup"><span data-stu-id="8cfd2-103">ISCrdEnr::enumCertTemplateName method</span></span>

<span data-ttu-id="8cfd2-104">Метод **енумцерттемплатенаме** перечисляет имена шаблонов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-104">The **enumCertTemplateName** method enumerates the certificate template names.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cfd2-105">Syntax</span></span>


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="8cfd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cfd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cfd2-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cfd2-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfd2-108">Отсчитываемый от нуля индекс последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="8cfd2-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cfd2-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfd2-110">Значение, определяющее, применяется ли перечисленный шаблон сертификата к сертификатам пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-110">A value that determines whether the enumerated certificate template applies to user or machine certificates.</span></span> <span data-ttu-id="8cfd2-111">Если это значение равно бросить \_ зарегистрировать \_ \_ шаблон сертификата пользователя \_ (определяется как 1), то перечисление применяется к шаблонам сертификатов пользователей.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-111">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1), the enumeration applies to user certificate templates.</span></span> <span data-ttu-id="8cfd2-112">Если это значение равно бросить \_ зарегистрировать \_ \_ шаблон сертификата компьютера \_ (определяется как 2), то перечисление применяется к шаблонам сертификатов компьютера.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-112">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2), the enumeration applies to machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="8cfd2-113">*пбстрцерттемплатенаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8cfd2-113">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cfd2-114">Указатель на строку, которая возвращает имя перечисленного шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-114">A pointer to a string that returns the name of the enumerated certificate template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cfd2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cfd2-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="8cfd2-116">C++</span><span class="sxs-lookup"><span data-stu-id="8cfd2-116">C++</span></span>

<span data-ttu-id="8cfd2-117">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="8cfd2-118">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="8cfd2-119">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="8cfd2-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="8cfd2-120">VB</span><span class="sxs-lookup"><span data-stu-id="8cfd2-120">VB</span></span>

<span data-ttu-id="8cfd2-121">Строка, содержащая имя перечисленного шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-121">A string that contains the name of the enumerated certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfd2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8cfd2-122">Requirements</span></span>



| <span data-ttu-id="8cfd2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8cfd2-123">Requirement</span></span> | <span data-ttu-id="8cfd2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8cfd2-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfd2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cfd2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8cfd2-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8cfd2-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8cfd2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cfd2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8cfd2-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cfd2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8cfd2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8cfd2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cfd2-130"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cfd2-130"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="8cfd2-131">IID</span><span class="sxs-lookup"><span data-stu-id="8cfd2-131">IID</span></span><br/>                      | <span data-ttu-id="8cfd2-132">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="8cfd2-132">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8cfd2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cfd2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfd2-134">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-134">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="8cfd2-135">**Искрденр:: Жетцерттемплатекаунт**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-135">**ISCrdEnr::getCertTemplateCount**</span></span>](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[<span data-ttu-id="8cfd2-136">**Искрденр:: Жетцерттемплатенаме**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-136">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[<span data-ttu-id="8cfd2-137">**Искрденр:: Сетцерттемплатенаме**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-137">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




