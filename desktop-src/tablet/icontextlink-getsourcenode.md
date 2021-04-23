---
description: Извлекает объект Иконтекстноде, являющийся источником для этого Иконтекстлинк.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'Метод Иконтекстлинк:: Жетсаурценоде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eddab21740bf30c67e247cec89723bc47cd9dca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263151"
---
# <a name="icontextlinkgetsourcenode-method"></a><span data-ttu-id="11933-103">Метод Иконтекстлинк:: Жетсаурценоде</span><span class="sxs-lookup"><span data-stu-id="11933-103">IContextLink::GetSourceNode method</span></span>

<span data-ttu-id="11933-104">Извлекает объект [**иконтекстноде**](icontextnode.md) , являющийся источником для этого [**иконтекстлинк**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="11933-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="11933-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11933-105">Syntax</span></span>


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="11933-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11933-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11933-107">*ппсркконтекстнодеид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11933-107">*ppSrcContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11933-108">Указатель на объект [**иконтекстноде**](icontextnode.md) , являющийся источником для этого [**иконтекстлинк**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="11933-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11933-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11933-109">Return value</span></span>

<span data-ttu-id="11933-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="11933-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11933-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11933-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="11933-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппсркконтекстнодеид* , когда больше не нужно использовать исходный узел.</span><span class="sxs-lookup"><span data-stu-id="11933-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSrcContextNodeId* when you no longer need to use the source node.</span></span>

 

<span data-ttu-id="11933-113">Если объект [**иконтекстлинк**](icontextlink.md) связан между узлом, который содержит запись, и узлом, содержащим рисование, то исходный узел обычно является узлом, содержащим рисование.</span><span class="sxs-lookup"><span data-stu-id="11933-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the source node is generally the node that contains drawing.</span></span>

<span data-ttu-id="11933-114">Если объект [**иконтекстлинк**](icontextlink.md) имеет тип ссылки, включающий (см. [**Иконтекстлинк:: жетконтекстлинкдиректион**](icontextlink-getcontextlinkdirection.md)), то исходный узел является узлом, который заключает в себя узел назначения.</span><span class="sxs-lookup"><span data-stu-id="11933-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the source node is the node that encloses the destination node.</span></span>

## <a name="requirements"></a><span data-ttu-id="11933-115">Требования</span><span class="sxs-lookup"><span data-stu-id="11933-115">Requirements</span></span>



| <span data-ttu-id="11933-116">Требование</span><span class="sxs-lookup"><span data-stu-id="11933-116">Requirement</span></span> | <span data-ttu-id="11933-117">Значение</span><span class="sxs-lookup"><span data-stu-id="11933-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11933-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11933-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11933-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="11933-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11933-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11933-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11933-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="11933-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="11933-122">Header</span><span class="sxs-lookup"><span data-stu-id="11933-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11933-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="11933-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="11933-124">DLL</span><span class="sxs-lookup"><span data-stu-id="11933-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11933-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11933-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="11933-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11933-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11933-127">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="11933-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="11933-128">**Иконтекстлинк:: Жетдестинатионноде**</span><span class="sxs-lookup"><span data-stu-id="11933-128">**IContextLink::GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)
</dt> <dt>

[<span data-ttu-id="11933-129">**контекстлинкдиректион**</span><span class="sxs-lookup"><span data-stu-id="11933-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="11933-130">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="11933-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

