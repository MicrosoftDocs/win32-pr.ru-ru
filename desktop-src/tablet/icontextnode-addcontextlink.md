---
description: Добавляет новый Иконтекстлинк в коллекцию ссылок контекста объекта Иконтекстноде.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'Метод Иконтекстноде:: Аддконтекстлинк (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650551"
---
# <a name="icontextnodeaddcontextlink-method"></a><span data-ttu-id="c679a-103">Метод Иконтекстноде:: Аддконтекстлинк</span><span class="sxs-lookup"><span data-stu-id="c679a-103">IContextNode::AddContextLink method</span></span>

<span data-ttu-id="c679a-104">Добавляет новый [**иконтекстлинк**](icontextlink.md) в коллекцию ссылок контекста объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="c679a-104">Adds a new [**IContextLink**](icontextlink.md) to the [**IContextNode**](icontextnode.md) object's collection of context links.</span></span>

## <a name="syntax"></a><span data-ttu-id="c679a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c679a-105">Syntax</span></span>


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a><span data-ttu-id="c679a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c679a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c679a-107">*пдестинатионноде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c679a-107">*pDestinationNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c679a-108">Целевой [**иконтекстноде**](icontextnode.md) для нового [**иконтекстлинк**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="c679a-108">The destination [**IContextNode**](icontextnode.md) for the new [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="c679a-109">*линкдиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c679a-109">*linkDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c679a-110">Направление создаваемого объекта [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="c679a-110">The direction of [**IContextLink**](icontextlink.md) object to create.</span></span>

</dd> <dt>

<span data-ttu-id="c679a-111">*ппконтекстлинктоадд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c679a-111">*ppContextLinkToAdd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c679a-112">Указатель на новый объект [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="c679a-112">A pointer to the new [**IContextLink**](icontextlink.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c679a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c679a-113">Return value</span></span>

<span data-ttu-id="c679a-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c679a-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c679a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c679a-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c679a-116">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстлинктоадд* , когда больше не нужно использовать контекстный узел.</span><span class="sxs-lookup"><span data-stu-id="c679a-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinkToAdd* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="c679a-117">Этот объект [**иконтекстноде**](icontextnode.md) является исходным узлом (см. [**Иконтекстлинк:: жетсаурценоде**](icontextlink-getsourcenode.md)) для нового объекта [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="c679a-117">This [**IContextNode**](icontextnode.md) object is the source node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) for the new [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c679a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c679a-118">Requirements</span></span>



| <span data-ttu-id="c679a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c679a-119">Requirement</span></span> | <span data-ttu-id="c679a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c679a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c679a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c679a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c679a-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c679a-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c679a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c679a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c679a-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c679a-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c679a-125">Header</span><span class="sxs-lookup"><span data-stu-id="c679a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c679a-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c679a-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c679a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c679a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c679a-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c679a-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c679a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c679a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c679a-130">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="c679a-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c679a-131">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="c679a-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="c679a-132">**иконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="c679a-132">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="c679a-133">**контекстлинкдиректион**</span><span class="sxs-lookup"><span data-stu-id="c679a-133">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="c679a-134">**Иконтекстноде::D Елетеконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="c679a-134">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="c679a-135">**Иконтекстноде:: Жетконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="c679a-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="c679a-136">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="c679a-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

