---
description: Извлекает коллекцию объектов Иконтекстлинк, представляющих связи с другими объектами Иконтекстноде.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'Метод Иконтекстноде:: Жетконтекстлинкс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650548"
---
# <a name="icontextnodegetcontextlinks-method"></a><span data-ttu-id="42474-103">Метод Иконтекстноде:: Жетконтекстлинкс</span><span class="sxs-lookup"><span data-stu-id="42474-103">IContextNode::GetContextLinks method</span></span>

<span data-ttu-id="42474-104">Извлекает коллекцию объектов [**иконтекстлинк**](icontextlink.md) , представляющих связи с другими объектами [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="42474-104">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="42474-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42474-105">Syntax</span></span>


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a><span data-ttu-id="42474-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42474-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42474-107">*ппконтекстлинкс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="42474-107">*ppContextLinks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42474-108">Указатель на коллекцию объектов [**иконтекстлинк**](icontextlink.md) , представляющих связи с другими объектами [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="42474-108">A pointer to a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42474-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42474-109">Return value</span></span>

<span data-ttu-id="42474-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="42474-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="42474-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42474-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="42474-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстлинкс* , когда больше не нужно использовать коллекцию ссылок контекста.</span><span class="sxs-lookup"><span data-stu-id="42474-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinks* when you no longer need to use the context links collection.</span></span>

 

<span data-ttu-id="42474-113">Чтобы получить сведения о связях между родительскими или дочерними узлами, используйте [**иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) или [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md).</span><span class="sxs-lookup"><span data-stu-id="42474-113">To get information about parent or child node relationships, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) or [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).</span></span>

<span data-ttu-id="42474-114">Дополнительные сведения о видах связей, описываемых ссылками, см. в разделе [**иконтекстлинк**](icontextlink.md) и [**контекстлинкдиректион**](contextlinkdirection.md).</span><span class="sxs-lookup"><span data-stu-id="42474-114">For more information about the kinds of relationships that are described by links, see [**IContextLink**](icontextlink.md) and [**ContextLinkDirection**](contextlinkdirection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42474-115">Требования</span><span class="sxs-lookup"><span data-stu-id="42474-115">Requirements</span></span>



| <span data-ttu-id="42474-116">Требование</span><span class="sxs-lookup"><span data-stu-id="42474-116">Requirement</span></span> | <span data-ttu-id="42474-117">Значение</span><span class="sxs-lookup"><span data-stu-id="42474-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42474-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42474-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42474-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="42474-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="42474-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42474-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42474-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="42474-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="42474-122">Header</span><span class="sxs-lookup"><span data-stu-id="42474-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="42474-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="42474-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="42474-124">DLL</span><span class="sxs-lookup"><span data-stu-id="42474-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42474-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42474-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="42474-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42474-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42474-127">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="42474-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="42474-128">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="42474-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="42474-129">**контекстлинкдиректион**</span><span class="sxs-lookup"><span data-stu-id="42474-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="42474-130">**Иконтекстноде:: Аддконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="42474-130">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="42474-131">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="42474-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

