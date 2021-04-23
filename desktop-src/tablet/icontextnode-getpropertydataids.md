---
description: Возвращает идентификаторы, для которых имеются данные свойств.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'Метод Иконтекстноде:: Жетпропертидатаидс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719346"
---
# <a name="icontextnodegetpropertydataids-method"></a><span data-ttu-id="56216-103">Метод Иконтекстноде:: Жетпропертидатаидс</span><span class="sxs-lookup"><span data-stu-id="56216-103">IContextNode::GetPropertyDataIds method</span></span>

<span data-ttu-id="56216-104">Возвращает идентификаторы, для которых имеются данные свойств.</span><span class="sxs-lookup"><span data-stu-id="56216-104">Retrieves the identifiers for which there is property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="56216-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56216-105">Syntax</span></span>


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a><span data-ttu-id="56216-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56216-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56216-107">*пулгуидкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="56216-107">*pulGuidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56216-108">Количество свойств.</span><span class="sxs-lookup"><span data-stu-id="56216-108">The number of properties.</span></span>

</dd> <dt>

<span data-ttu-id="56216-109">*ппгуидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="56216-109">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56216-110">Идентификаторы, для которых имеются данные свойств.</span><span class="sxs-lookup"><span data-stu-id="56216-110">The identifiers for which there is property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56216-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56216-111">Return value</span></span>

<span data-ttu-id="56216-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="56216-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="56216-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56216-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="56216-114">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппгуидс* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="56216-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="56216-115">Этот метод возвращает идентификаторы конкретного приложения для добавленных данных свойства.</span><span class="sxs-lookup"><span data-stu-id="56216-115">This method returns the application-specific identifiers for property data that has been added.</span></span> <span data-ttu-id="56216-116">Он также возвращает идентификаторы для внутренних данных свойства, которые описаны константами [свойств узла контекста](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="56216-116">It also returns the identifiers for the internal property data, which are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="56216-117">Требования</span><span class="sxs-lookup"><span data-stu-id="56216-117">Requirements</span></span>



| <span data-ttu-id="56216-118">Требование</span><span class="sxs-lookup"><span data-stu-id="56216-118">Requirement</span></span> | <span data-ttu-id="56216-119">Значение</span><span class="sxs-lookup"><span data-stu-id="56216-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56216-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56216-120">Minimum supported client</span></span><br/> | <span data-ttu-id="56216-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="56216-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="56216-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56216-122">Minimum supported server</span></span><br/> | <span data-ttu-id="56216-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="56216-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="56216-124">Header</span><span class="sxs-lookup"><span data-stu-id="56216-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="56216-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="56216-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="56216-126">DLL</span><span class="sxs-lookup"><span data-stu-id="56216-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56216-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56216-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="56216-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56216-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56216-129">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="56216-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="56216-130">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="56216-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="56216-131">**Иконтекстноде:: Контаинспропертидата**</span><span class="sxs-lookup"><span data-stu-id="56216-131">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="56216-132">**Иконтекстноде:: Ремовепропертидата**</span><span class="sxs-lookup"><span data-stu-id="56216-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="56216-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="56216-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

