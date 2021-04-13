---
description: Метод Item объекта Свбемнамедвалуесет получает объект Свбемнамедвалуе из коллекции.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: Метод Свбемнамедвалуесет. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544663"
---
# <a name="swbemnamedvaluesetitem-method"></a><span data-ttu-id="db60b-103">Свбемнамедвалуесет. Item, метод</span><span class="sxs-lookup"><span data-stu-id="db60b-103">SWbemNamedValueSet.Item method</span></span>

<span data-ttu-id="db60b-104">Метод **Item** объекта [**Свбемнамедвалуесет**](swbemnamedvalueset.md) получает объект [**свбемнамедвалуе**](swbemnamedvalue.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="db60b-104">The **Item** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object gets an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span>

<span data-ttu-id="db60b-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="db60b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="db60b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db60b-106">Syntax</span></span>


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="db60b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="db60b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db60b-108">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db60b-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db60b-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="db60b-109">Required.</span></span> <span data-ttu-id="db60b-110">Имя извлекаемого значения.</span><span class="sxs-lookup"><span data-stu-id="db60b-110">Name of the value to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="db60b-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="db60b-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db60b-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="db60b-112">Reserved.</span></span> <span data-ttu-id="db60b-113">Если указано, это значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="db60b-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db60b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db60b-114">Return value</span></span>

<span data-ttu-id="db60b-115">В случае успешного выполнения возвращается запрошенный объект [**свбемнамедвалуе**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="db60b-115">If successful, the requested [**SWbemNamedValue**](swbemnamedvalue.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db60b-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="db60b-116">Error codes</span></span>

<span data-ttu-id="db60b-117">После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="db60b-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="db60b-118">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="db60b-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="db60b-119">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="db60b-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="db60b-120">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="db60b-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="db60b-121">Указан недопустимый параметр, или не удалось выполнить синтаксический анализ пространства имен.</span><span class="sxs-lookup"><span data-stu-id="db60b-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="db60b-122">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="db60b-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="db60b-123">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="db60b-123">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="db60b-124">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="db60b-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="db60b-125">Запрашиваемый элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="db60b-125">The requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db60b-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db60b-126">Remarks</span></span>

<span data-ttu-id="db60b-127">Примеры добавления и получения именованных значений см. в разделе [**свбемнамедвалуе. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="db60b-127">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db60b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="db60b-128">Requirements</span></span>



| <span data-ttu-id="db60b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="db60b-129">Requirement</span></span> | <span data-ttu-id="db60b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="db60b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db60b-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db60b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="db60b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db60b-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db60b-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db60b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="db60b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db60b-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db60b-135">Header</span><span class="sxs-lookup"><span data-stu-id="db60b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="db60b-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db60b-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="db60b-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="db60b-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="db60b-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="db60b-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="db60b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="db60b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db60b-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db60b-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="db60b-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="db60b-141">CLSID</span></span><br/>                    | <span data-ttu-id="db60b-142">\_СВБЕМНАМЕДВАЛУЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="db60b-142">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="db60b-143">IID</span><span class="sxs-lookup"><span data-stu-id="db60b-143">IID</span></span><br/>                      | <span data-ttu-id="db60b-144">IID \_ исвбемнамедвалуесет</span><span class="sxs-lookup"><span data-stu-id="db60b-144">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="db60b-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db60b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db60b-146">**свбемнамедвалуесет**</span><span class="sxs-lookup"><span data-stu-id="db60b-146">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




