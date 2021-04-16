---
description: Возвращает число центров сертификации (CAs), которые хотят выдать сертификат на основе указанного шаблона сертификата.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'Метод Искрденр:: Жеткакаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664399"
---
# <a name="iscrdenrgetcacount-method"></a><span data-ttu-id="15637-103">Метод Искрденр:: Жеткакаунт</span><span class="sxs-lookup"><span data-stu-id="15637-103">ISCrdEnr::getCACount method</span></span>

<span data-ttu-id="15637-104">Метод **жеткакаунт** возвращает число [*центров сертификации*](../secgloss/c-gly.md) (CAS), которые хотят выдать сертификат на основе указанного шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="15637-104">The **getCACount** method returns the number of [*certification authorities*](../secgloss/c-gly.md) (CAs) willing to issue a certificate based on the specified certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="15637-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15637-105">Syntax</span></span>


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a><span data-ttu-id="15637-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15637-107">*бстрцерттемплатенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15637-107">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15637-108">Строка, представляющая имя шаблона сертификата.</span><span class="sxs-lookup"><span data-stu-id="15637-108">A string that represents the name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="15637-109">*пдвкакаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="15637-109">*pdwCACount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15637-110">Указатель на значение **типа Long** , возвращающее количество доступных центров сертификации, которые выдают сертификат для шаблона сертификата, указанного в *бстрцерттемплатенаме*.</span><span class="sxs-lookup"><span data-stu-id="15637-110">A pointer to a **LONG** that returns the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15637-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15637-111">Return value</span></span>

### <a name="c"></a><span data-ttu-id="15637-112">C++</span><span class="sxs-lookup"><span data-stu-id="15637-112">C++</span></span>

<span data-ttu-id="15637-113">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="15637-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="15637-114">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="15637-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="15637-115">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="15637-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="15637-116">VB</span><span class="sxs-lookup"><span data-stu-id="15637-116">VB</span></span>

<span data-ttu-id="15637-117">Значение **типа Long** , представляющее количество доступных центров сертификации, которые будут выдавать сертификат для шаблона сертификата, указанного в *бстрцерттемплатенаме*.</span><span class="sxs-lookup"><span data-stu-id="15637-117">A **Long** value that represents the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

## <a name="requirements"></a><span data-ttu-id="15637-118">Требования</span><span class="sxs-lookup"><span data-stu-id="15637-118">Requirements</span></span>



| <span data-ttu-id="15637-119">Требование</span><span class="sxs-lookup"><span data-stu-id="15637-119">Requirement</span></span> | <span data-ttu-id="15637-120">Значение</span><span class="sxs-lookup"><span data-stu-id="15637-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15637-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15637-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15637-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="15637-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="15637-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15637-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15637-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="15637-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15637-125">DLL</span><span class="sxs-lookup"><span data-stu-id="15637-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15637-126"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15637-126"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="15637-127">IID</span><span class="sxs-lookup"><span data-stu-id="15637-127">IID</span></span><br/>                      | <span data-ttu-id="15637-128">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="15637-128">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="15637-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15637-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15637-130">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="15637-130">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="15637-131">**Искрденр:: Енумканаме**</span><span class="sxs-lookup"><span data-stu-id="15637-131">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="15637-132">**Искрденр:: Жетканаме**</span><span class="sxs-lookup"><span data-stu-id="15637-132">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
