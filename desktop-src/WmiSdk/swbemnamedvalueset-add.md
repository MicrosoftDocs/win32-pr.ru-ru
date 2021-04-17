---
description: Метод Add объекта Свбемнамедвалуесет добавляет объект Свбемнамедвалуе в коллекцию. Если элемент уже существует в коллекции с тем же именем, новый элемент заменяет его.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Метод Свбемнамедвалуесет. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544666"
---
# <a name="swbemnamedvaluesetadd-method"></a><span data-ttu-id="d53b6-104">Свбемнамедвалуесет. Add, метод</span><span class="sxs-lookup"><span data-stu-id="d53b6-104">SWbemNamedValueSet.Add method</span></span>

<span data-ttu-id="d53b6-105">Метод **Add** объекта [**Свбемнамедвалуесет**](swbemnamedvalueset.md) добавляет объект [**свбемнамедвалуе**](swbemnamedvalue.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="d53b6-105">The **Add** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span> <span data-ttu-id="d53b6-106">Если элемент уже существует в коллекции с тем же именем, новый элемент заменяет его.</span><span class="sxs-lookup"><span data-stu-id="d53b6-106">If an element already exists in the collection with the same name, the new element replaces it.</span></span>

<span data-ttu-id="d53b6-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d53b6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d53b6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d53b6-108">Syntax</span></span>


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d53b6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d53b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d53b6-110">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d53b6-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d53b6-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d53b6-111">Required.</span></span> <span data-ttu-id="d53b6-112">Имя нового значения.</span><span class="sxs-lookup"><span data-stu-id="d53b6-112">Name of the new value.</span></span>

</dd> <dt>

<span data-ttu-id="d53b6-113">*варвал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d53b6-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d53b6-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d53b6-114">Required.</span></span> <span data-ttu-id="d53b6-115">Вариант, представляющий новое значение.</span><span class="sxs-lookup"><span data-stu-id="d53b6-115">Variant that represents the new value.</span></span>

</dd> <dt>

<span data-ttu-id="d53b6-116">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d53b6-116">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d53b6-117">Зарезервированные значения и должны быть равны нулю, если они заданы.</span><span class="sxs-lookup"><span data-stu-id="d53b6-117">Reserved and must be set to zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d53b6-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d53b6-118">Return value</span></span>

<span data-ttu-id="d53b6-119">В случае успешного выполнения этот метод возвращает недавно измененный или вновь созданный объект [**свбемнамедвалуе**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d53b6-119">If successful, this method returns the newly modified or newly created [**SWbemNamedValue**](swbemnamedvalue.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d53b6-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d53b6-120">Remarks</span></span>

<span data-ttu-id="d53b6-121">Примеры добавления и получения именованных значений см. в разделе [**свбемнамедвалуе. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="d53b6-121">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d53b6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d53b6-122">Requirements</span></span>



| <span data-ttu-id="d53b6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d53b6-123">Requirement</span></span> | <span data-ttu-id="d53b6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d53b6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d53b6-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d53b6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d53b6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d53b6-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d53b6-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d53b6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d53b6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d53b6-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d53b6-129">Header</span><span class="sxs-lookup"><span data-stu-id="d53b6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d53b6-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d53b6-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d53b6-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d53b6-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="d53b6-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d53b6-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d53b6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d53b6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d53b6-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d53b6-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d53b6-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="d53b6-135">CLSID</span></span><br/>                    | <span data-ttu-id="d53b6-136">\_СВБЕМНАМЕДВАЛУЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="d53b6-136">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="d53b6-137">IID</span><span class="sxs-lookup"><span data-stu-id="d53b6-137">IID</span></span><br/>                      | <span data-ttu-id="d53b6-138">IID \_ исвбемнамедвалуесет</span><span class="sxs-lookup"><span data-stu-id="d53b6-138">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="d53b6-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d53b6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d53b6-140">**свбемнамедвалуесет**</span><span class="sxs-lookup"><span data-stu-id="d53b6-140">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




