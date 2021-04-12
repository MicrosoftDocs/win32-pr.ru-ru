---
title: Свойство Counters. Item
description: Извлекает указанный экземпляр Каунтеритем из коллекции.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Свойство элемента Сисмон
- Свойство Item Сисмон, класс Counters
- Счетчики класса Сисмон, свойство Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489717"
---
# <a name="countersitem-property"></a><span data-ttu-id="61199-106">Свойство Counters. Item</span><span class="sxs-lookup"><span data-stu-id="61199-106">Counters.Item property</span></span>

<span data-ttu-id="61199-107">Извлекает указанный экземпляр [**каунтеритем**](counteritem.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="61199-107">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span>

<span data-ttu-id="61199-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="61199-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61199-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61199-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a><span data-ttu-id="61199-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="61199-110">Property value</span></span>

<span data-ttu-id="61199-111">Экземпляр [**каунтеритем**](counteritem.md) , соответствующий указанному значению индекса.</span><span class="sxs-lookup"><span data-stu-id="61199-111">[**CounterItem**](counteritem.md) instance that corresponds to the specified index value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="61199-112">Исключения</span><span class="sxs-lookup"><span data-stu-id="61199-112">Exceptions</span></span>



| <span data-ttu-id="61199-113">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="61199-113">Exception type</span></span>                                  | <span data-ttu-id="61199-114">Условие</span><span class="sxs-lookup"><span data-stu-id="61199-114">Condition</span></span>                         |
|-------------------------------------------------|-----------------------------------|
| <span data-ttu-id="61199-115">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="61199-115">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="61199-116">Указан недопустимый индекс.</span><span class="sxs-lookup"><span data-stu-id="61199-116">The specified index is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="61199-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61199-117">Remarks</span></span>

<span data-ttu-id="61199-118">Это свойство объекта [**Counters**](counters.md) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61199-118">This is the default property of the [**Counters**](counters.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="61199-119">Требования</span><span class="sxs-lookup"><span data-stu-id="61199-119">Requirements</span></span>



| <span data-ttu-id="61199-120">Требование</span><span class="sxs-lookup"><span data-stu-id="61199-120">Requirement</span></span> | <span data-ttu-id="61199-121">Значение</span><span class="sxs-lookup"><span data-stu-id="61199-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61199-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61199-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61199-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61199-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="61199-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61199-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61199-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61199-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61199-126">DLL</span><span class="sxs-lookup"><span data-stu-id="61199-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61199-127"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="61199-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61199-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61199-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61199-129">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="61199-129">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="61199-130">**Счетчики**</span><span class="sxs-lookup"><span data-stu-id="61199-130">**Counters**</span></span>](counters.md)
</dt> </dl>

 

 





