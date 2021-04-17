---
description: Удаляет объект Иконтекстлинк из коллекции ссылок объекта Иконтекстноде.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: 'Иконтекстноде: метод:D Елетеконтекстлинк (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711137"
---
# <a name="icontextnodedeletecontextlink-method"></a><span data-ttu-id="8b321-103">Иконтекстноде: метод:D Елетеконтекстлинк</span><span class="sxs-lookup"><span data-stu-id="8b321-103">IContextNode::DeleteContextLink method</span></span>

<span data-ttu-id="8b321-104">Удаляет объект [**иконтекстлинк**](icontextlink.md) из коллекции ссылок объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="8b321-104">Deletes an [**IContextLink**](icontextlink.md) object from the [**IContextNode**](icontextnode.md) object's link collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b321-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b321-105">Syntax</span></span>


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="8b321-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b321-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b321-107">*пконтекстлинктоделете* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8b321-107">*pContextLinkToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b321-108">Удаляемый объект [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="8b321-108">The [**IContextLink**](icontextlink.md) object to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b321-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b321-109">Return value</span></span>

<span data-ttu-id="8b321-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8b321-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b321-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b321-111">Remarks</span></span>

<span data-ttu-id="8b321-112">Ссылка на контекст имеет исходный узел и узел назначения (см. раздел [**иконтекстлинк:: жетсаурценоде**](icontextlink-getsourcenode.md) and [**Иконтекстлинк:: жетдестинатионноде**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="8b321-112">A context link has a source node and a destination node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span> <span data-ttu-id="8b321-113">Этот метод удаляет [**иконтекстлинк**](icontextlink.md) из коллекции ссылок на исходный и конечный узлы (см. раздел [**Иконтекстноде:: жетконтекстлинкс**](icontextnode-getcontextlinks.md)).</span><span class="sxs-lookup"><span data-stu-id="8b321-113">This method removes the [**IContextLink**](icontextlink.md) from both the source and destination nodes' collection of context links (see [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b321-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8b321-114">Requirements</span></span>



| <span data-ttu-id="8b321-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8b321-115">Requirement</span></span> | <span data-ttu-id="8b321-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8b321-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b321-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b321-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b321-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8b321-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8b321-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b321-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b321-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8b321-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8b321-121">Header</span><span class="sxs-lookup"><span data-stu-id="8b321-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b321-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8b321-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8b321-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8b321-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b321-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b321-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8b321-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b321-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b321-126">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="8b321-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8b321-127">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="8b321-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="8b321-128">**Иконтекстноде:: Аддконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="8b321-128">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="8b321-129">**Иконтекстноде:: Жетконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="8b321-129">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="8b321-130">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="8b321-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




