---
description: Метод Item объекта SWbemPropertySet получает именованный SWbemProperty из коллекции. Это метод по умолчанию для этого объекта.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: Метод SWbemPropertySet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272556"
---
# <a name="swbempropertysetitem-method"></a><span data-ttu-id="ea761-104">SWbemPropertySet. Item, метод</span><span class="sxs-lookup"><span data-stu-id="ea761-104">SWbemPropertySet.Item method</span></span>

<span data-ttu-id="ea761-105">Метод **Item** объекта [**SWbemPropertySet**](swbempropertyset.md) получает именованный [**SWbemProperty**](swbemproperty.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="ea761-105">The **Item** method of the [**SWbemPropertySet**](swbempropertyset.md) object gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="ea761-106">Это метод по умолчанию для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="ea761-106">This is the default method for this object.</span></span>

<span data-ttu-id="ea761-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ea761-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea761-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea761-108">Syntax</span></span>


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ea761-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea761-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea761-110">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ea761-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea761-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ea761-111">Required.</span></span> <span data-ttu-id="ea761-112">Имя извлекаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="ea761-112">Name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ea761-113">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ea761-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea761-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ea761-114">Reserved.</span></span> <span data-ttu-id="ea761-115">Если указано, это значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ea761-115">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea761-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea761-116">Return value</span></span>

<span data-ttu-id="ea761-117">В случае успешного выполнения возвращается запрошенный объект [**SWbemProperty**](swbemproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ea761-117">If successful, the requested [**SWbemProperty**](swbemproperty.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ea761-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ea761-118">Error codes</span></span>

<span data-ttu-id="ea761-119">После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="ea761-119">After the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ea761-120">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ea761-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ea761-121">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="ea761-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="ea761-122">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ea761-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ea761-123">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ea761-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="ea761-124">**вбемерраутофмемори** -2147749896</span><span class="sxs-lookup"><span data-stu-id="ea761-124">**wbemErrOutOfMemory** - 2147749896</span></span>
</dt> <dd>

<span data-ttu-id="ea761-125">Недостаточно памяти для выполнения этого метода.</span><span class="sxs-lookup"><span data-stu-id="ea761-125">Not enough memory for this method to execute.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea761-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ea761-126">Requirements</span></span>



| <span data-ttu-id="ea761-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ea761-127">Requirement</span></span> | <span data-ttu-id="ea761-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ea761-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea761-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea761-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ea761-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea761-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea761-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea761-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ea761-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea761-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea761-133">Header</span><span class="sxs-lookup"><span data-stu-id="ea761-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea761-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea761-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea761-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ea761-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea761-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ea761-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ea761-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ea761-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea761-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea761-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea761-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="ea761-139">CLSID</span></span><br/>                    | <span data-ttu-id="ea761-140">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="ea761-140">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="ea761-141">IID</span><span class="sxs-lookup"><span data-stu-id="ea761-141">IID</span></span><br/>                      | <span data-ttu-id="ea761-142">IID \_ исвбемпропертисет</span><span class="sxs-lookup"><span data-stu-id="ea761-142">IID\_ISWbemPropertySet</span></span><br/>                                                       |



 

 




