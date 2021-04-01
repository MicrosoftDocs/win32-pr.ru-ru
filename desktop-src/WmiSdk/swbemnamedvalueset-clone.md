---
description: Метод Clone объекта Свбемнамедвалуесет возвращает новый объект, который является клоном текущей коллекции.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Метод Свбемнамедвалуесет. Clone (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814321"
---
# <a name="swbemnamedvaluesetclone-method"></a><span data-ttu-id="3f70c-103">Свбемнамедвалуесет. Clone, метод</span><span class="sxs-lookup"><span data-stu-id="3f70c-103">SWbemNamedValueSet.Clone method</span></span>

<span data-ttu-id="3f70c-104">Метод **clone** объекта [**свбемнамедвалуесет**](swbemnamedvalueset.md) возвращает новый объект, который является клоном текущей коллекции.</span><span class="sxs-lookup"><span data-stu-id="3f70c-104">The **Clone** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns a new object that is a clone of the current collection.</span></span>

<span data-ttu-id="3f70c-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3f70c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f70c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f70c-106">Syntax</span></span>


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a><span data-ttu-id="3f70c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f70c-107">Parameters</span></span>

<span data-ttu-id="3f70c-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3f70c-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f70c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f70c-109">Return value</span></span>

<span data-ttu-id="3f70c-110">В случае успешного выполнения новый объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3f70c-110">If successful, a new [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3f70c-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3f70c-111">Error codes</span></span>

<span data-ttu-id="3f70c-112">После завершения метода **clone** объект **Err** может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="3f70c-112">Upon completion of the **Clone** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="3f70c-113">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="3f70c-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="3f70c-114">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3f70c-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="3f70c-115">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="3f70c-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="3f70c-116">Недостаточно памяти для клонирования объекта.</span><span class="sxs-lookup"><span data-stu-id="3f70c-116">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f70c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f70c-117">Remarks</span></span>

<span data-ttu-id="3f70c-118">Используйте этот метод для дублирования коллекции [**свбемнамедвалуесет**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="3f70c-118">Use this method to duplicate an [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f70c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3f70c-119">Requirements</span></span>



| <span data-ttu-id="3f70c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3f70c-120">Requirement</span></span> | <span data-ttu-id="3f70c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3f70c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f70c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f70c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3f70c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f70c-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3f70c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f70c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3f70c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f70c-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3f70c-126">Header</span><span class="sxs-lookup"><span data-stu-id="3f70c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f70c-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f70c-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f70c-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3f70c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f70c-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f70c-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f70c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3f70c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f70c-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f70c-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f70c-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="3f70c-132">CLSID</span></span><br/>                    | <span data-ttu-id="3f70c-133">\_СВБЕМНАМЕДВАЛУЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="3f70c-133">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="3f70c-134">IID</span><span class="sxs-lookup"><span data-stu-id="3f70c-134">IID</span></span><br/>                      | <span data-ttu-id="3f70c-135">IID \_ исвбемнамедвалуесет</span><span class="sxs-lookup"><span data-stu-id="3f70c-135">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="3f70c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f70c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f70c-137">**свбемнамедвалуесет**</span><span class="sxs-lookup"><span data-stu-id="3f70c-137">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




