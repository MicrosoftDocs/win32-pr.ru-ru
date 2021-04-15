---
description: Определяет, содержит ли объект Иконтекстноде данные, хранящиеся по указанному идентификатору.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'Метод Иконтекстноде:: Контаинспропертидата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497589"
---
# <a name="icontextnodecontainspropertydata-method"></a><span data-ttu-id="f58e2-103">Метод Иконтекстноде:: Контаинспропертидата</span><span class="sxs-lookup"><span data-stu-id="f58e2-103">IContextNode::ContainsPropertyData method</span></span>

<span data-ttu-id="f58e2-104">Определяет, содержит ли объект [**иконтекстноде**](icontextnode.md) данные, хранящиеся по указанному идентификатору.</span><span class="sxs-lookup"><span data-stu-id="f58e2-104">Determines whether the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="f58e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f58e2-105">Syntax</span></span>


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a><span data-ttu-id="f58e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f58e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f58e2-107">*ппропертидатаид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f58e2-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f58e2-108">Идентификатор данных.</span><span class="sxs-lookup"><span data-stu-id="f58e2-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="f58e2-109">*пбконтаинс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f58e2-109">*pbContains* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f58e2-110">**Вариант \_ Значение TRUE** , если объект [**иконтекстноде**](icontextnode.md) содержит данные, хранящиеся по указанному идентификатору; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="f58e2-110">**VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f58e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f58e2-111">Return value</span></span>

<span data-ttu-id="f58e2-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f58e2-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f58e2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f58e2-113">Remarks</span></span>

<span data-ttu-id="f58e2-114">Кроме данных, относящихся к конкретному приложению, этот метод можно использовать для определения того, содержит ли [**иконтекстноде**](icontextnode.md) другие внутренние данные (см. раздел свойства указания по [анализу](analysis-hint-properties.md) и [Свойства узла контекста](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="f58e2-114">In addition to application-specific data, you can also use this method to determine whether this [**IContextNode**](icontextnode.md) contains other internal data (see [Analysis Hint Properties](analysis-hint-properties.md) and [Context Node Properties](context-node-properties.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f58e2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f58e2-115">Requirements</span></span>



| <span data-ttu-id="f58e2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f58e2-116">Requirement</span></span> | <span data-ttu-id="f58e2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f58e2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f58e2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f58e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f58e2-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f58e2-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f58e2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f58e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f58e2-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f58e2-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f58e2-122">Header</span><span class="sxs-lookup"><span data-stu-id="f58e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f58e2-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f58e2-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f58e2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f58e2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f58e2-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f58e2-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f58e2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f58e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f58e2-127">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="f58e2-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f58e2-128">**Иконтекстноде:: Аддпропертидата**</span><span class="sxs-lookup"><span data-stu-id="f58e2-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="f58e2-129">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="f58e2-129">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="f58e2-130">**Иконтекстноде:: Жетпропертидатаидс**</span><span class="sxs-lookup"><span data-stu-id="f58e2-130">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="f58e2-131">**Иконтекстноде:: Лоадпропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="f58e2-131">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="f58e2-132">**Иконтекстноде:: Ремовепропертидата**</span><span class="sxs-lookup"><span data-stu-id="f58e2-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="f58e2-133">**Иконтекстноде:: Савепропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="f58e2-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="f58e2-134">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="f58e2-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




