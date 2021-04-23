---
description: Извлекает объект Иконтекстноде, который является назначением для этого Иконтекстлинк.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'Метод Иконтекстлинк:: Жетдестинатионноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343725"
---
# <a name="icontextlinkgetdestinationnode-method"></a><span data-ttu-id="97d69-103">Метод Иконтекстлинк:: Жетдестинатионноде</span><span class="sxs-lookup"><span data-stu-id="97d69-103">IContextLink::GetDestinationNode method</span></span>

<span data-ttu-id="97d69-104">Извлекает объект [**иконтекстноде**](icontextnode.md) , который является назначением для этого [**иконтекстлинк**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="97d69-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97d69-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97d69-105">Syntax</span></span>


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="97d69-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97d69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d69-107">*ппдстконтекстнодеид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="97d69-107">*ppDstContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97d69-108">Указатель на объект [**иконтекстноде**](icontextnode.md) , который является назначением для этого [**иконтекстлинк**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="97d69-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d69-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97d69-109">Return value</span></span>

<span data-ttu-id="97d69-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="97d69-110">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97d69-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97d69-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="97d69-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппдстконтекстнодеид* , когда больше не нужно использовать узел назначения.</span><span class="sxs-lookup"><span data-stu-id="97d69-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppDstContextNodeId* when you no longer need to use the destination node.</span></span>

 

<span data-ttu-id="97d69-113">Если объект [**иконтекстлинк**](icontextlink.md) связан между узлом, который содержит запись, и узлом, содержащим рисование, узел назначения обычно является узлом, содержащим запись.</span><span class="sxs-lookup"><span data-stu-id="97d69-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the destination node is generally the node that contains writing.</span></span>

<span data-ttu-id="97d69-114">Если объект [**иконтекстлинк**](icontextlink.md) имеет тип ссылки, включающий (см. [**Иконтекстлинк:: жетконтекстлинкдиректион**](icontextlink-getcontextlinkdirection.md)), то узел назначения является объектом [**иконтекстноде**](icontextnode.md) , который является вложенным.</span><span class="sxs-lookup"><span data-stu-id="97d69-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the destination node is the [**IContextNode**](icontextnode.md) object that is enclosed.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d69-115">Требования</span><span class="sxs-lookup"><span data-stu-id="97d69-115">Requirements</span></span>



| <span data-ttu-id="97d69-116">Требование</span><span class="sxs-lookup"><span data-stu-id="97d69-116">Requirement</span></span> | <span data-ttu-id="97d69-117">Значение</span><span class="sxs-lookup"><span data-stu-id="97d69-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97d69-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97d69-118">Minimum supported client</span></span><br/> | <span data-ttu-id="97d69-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="97d69-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="97d69-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97d69-120">Minimum supported server</span></span><br/> | <span data-ttu-id="97d69-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="97d69-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="97d69-122">Header</span><span class="sxs-lookup"><span data-stu-id="97d69-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="97d69-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="97d69-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="97d69-124">DLL</span><span class="sxs-lookup"><span data-stu-id="97d69-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97d69-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d69-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="97d69-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97d69-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d69-127">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="97d69-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="97d69-128">**Иконтекстлинк:: Жетсаурценоде**</span><span class="sxs-lookup"><span data-stu-id="97d69-128">**IContextLink::GetSourceNode**</span></span>](icontextlink-getsourcenode.md)
</dt> <dt>

[<span data-ttu-id="97d69-129">**контекстлинкдиректион**</span><span class="sxs-lookup"><span data-stu-id="97d69-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="97d69-130">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="97d69-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

