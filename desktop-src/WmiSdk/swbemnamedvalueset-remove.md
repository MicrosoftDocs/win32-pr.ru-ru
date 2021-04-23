---
description: Метод Remove объекта Свбемнамедвалуесет удаляет именованное значение из контекста.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: Метод Свбемнамедвалуесет. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d41ecd7d28b95534c8e6d88d1c57756c269cf790
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702833"
---
# <a name="swbemnamedvaluesetremove-method"></a><span data-ttu-id="48909-103">Свбемнамедвалуесет. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="48909-103">SWbemNamedValueSet.Remove method</span></span>

<span data-ttu-id="48909-104">Метод **Remove** объекта [**свбемнамедвалуесет**](swbemnamedvalueset.md) удаляет именованное значение из контекста.</span><span class="sxs-lookup"><span data-stu-id="48909-104">The **Remove** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object deletes a named value from the context.</span></span>

<span data-ttu-id="48909-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="48909-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="48909-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48909-106">Syntax</span></span>


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="48909-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="48909-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48909-108">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48909-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48909-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="48909-109">Required.</span></span> <span data-ttu-id="48909-110">Имя удаляемого значения.</span><span class="sxs-lookup"><span data-stu-id="48909-110">Name of the value to remove.</span></span>

</dd> <dt>

<span data-ttu-id="48909-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="48909-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48909-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="48909-112">Reserved.</span></span> <span data-ttu-id="48909-113">Если указано, это значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="48909-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48909-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48909-114">Return value</span></span>

<span data-ttu-id="48909-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="48909-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48909-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="48909-116">Error codes</span></span>

<span data-ttu-id="48909-117">После завершения метода **Remove** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="48909-117">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="48909-118">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="48909-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="48909-119">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="48909-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="48909-120">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="48909-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="48909-121">Указан недопустимый параметр, или не удалось выполнить синтаксический анализ пространства имен.</span><span class="sxs-lookup"><span data-stu-id="48909-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="48909-122">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="48909-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="48909-123">Запрашиваемый элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="48909-123">The requested item was not found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48909-124">Требования</span><span class="sxs-lookup"><span data-stu-id="48909-124">Requirements</span></span>



| <span data-ttu-id="48909-125">Требование</span><span class="sxs-lookup"><span data-stu-id="48909-125">Requirement</span></span> | <span data-ttu-id="48909-126">Значение</span><span class="sxs-lookup"><span data-stu-id="48909-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48909-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48909-127">Minimum supported client</span></span><br/> | <span data-ttu-id="48909-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48909-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48909-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48909-129">Minimum supported server</span></span><br/> | <span data-ttu-id="48909-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48909-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48909-131">Header</span><span class="sxs-lookup"><span data-stu-id="48909-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="48909-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48909-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="48909-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="48909-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="48909-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="48909-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="48909-135">DLL</span><span class="sxs-lookup"><span data-stu-id="48909-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48909-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48909-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="48909-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="48909-137">CLSID</span></span><br/>                    | <span data-ttu-id="48909-138">\_СВБЕМНАМЕДВАЛУЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="48909-138">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="48909-139">IID</span><span class="sxs-lookup"><span data-stu-id="48909-139">IID</span></span><br/>                      | <span data-ttu-id="48909-140">IID \_ исвбемнамедвалуесет</span><span class="sxs-lookup"><span data-stu-id="48909-140">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="48909-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48909-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48909-142">**свбемнамедвалуесет**</span><span class="sxs-lookup"><span data-stu-id="48909-142">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




