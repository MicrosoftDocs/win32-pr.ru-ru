---
description: Представляет связь между двумя объектами Иконтекстноде.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Интерфейс Иконтекстлинк (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711139"
---
# <a name="icontextlink-interface"></a><span data-ttu-id="5a074-103">Интерфейс Иконтекстлинк</span><span class="sxs-lookup"><span data-stu-id="5a074-103">IContextLink interface</span></span>

<span data-ttu-id="5a074-104">Представляет связь между двумя объектами [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="5a074-104">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="5a074-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="5a074-105">Members</span></span>

<span data-ttu-id="5a074-106">Интерфейс **иконтекстлинк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5a074-106">The **IContextLink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5a074-107">**Иконтекстлинк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5a074-107">**IContextLink** also has these types of members:</span></span>

-   [<span data-ttu-id="5a074-108">Методы</span><span class="sxs-lookup"><span data-stu-id="5a074-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a074-109">Методы</span><span class="sxs-lookup"><span data-stu-id="5a074-109">Methods</span></span>

<span data-ttu-id="5a074-110">Интерфейс **иконтекстлинк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5a074-110">The **IContextLink** interface has these methods.</span></span>



| <span data-ttu-id="5a074-111">Метод</span><span class="sxs-lookup"><span data-stu-id="5a074-111">Method</span></span>                                                                  | <span data-ttu-id="5a074-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5a074-112">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a074-113">**жетконтекстлинкдиректион**</span><span class="sxs-lookup"><span data-stu-id="5a074-113">**GetContextLinkDirection**</span></span>](icontextlink-getcontextlinkdirection.md) | <span data-ttu-id="5a074-114">Извлекает тип отношения, представляемого этим **иконтекстлинк** .</span><span class="sxs-lookup"><span data-stu-id="5a074-114">Retrieves the type of relationship this **IContextLink** represents.</span></span><br/>                                         |
| [<span data-ttu-id="5a074-115">**жетдестинатионноде**</span><span class="sxs-lookup"><span data-stu-id="5a074-115">**GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)           | <span data-ttu-id="5a074-116">Извлекает объект [**иконтекстноде**](icontextnode.md) , который является назначением для этого **иконтекстлинк**.</span><span class="sxs-lookup"><span data-stu-id="5a074-116">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this **IContextLink**.</span></span><br/> |
| [<span data-ttu-id="5a074-117">**жетсаурценоде**</span><span class="sxs-lookup"><span data-stu-id="5a074-117">**GetSourceNode**</span></span>](icontextlink-getsourcenode.md)                     | <span data-ttu-id="5a074-118">Извлекает объект [**иконтекстноде**](icontextnode.md) , являющийся источником для этого **иконтекстлинк**.</span><span class="sxs-lookup"><span data-stu-id="5a074-118">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this **IContextLink**.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="5a074-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a074-119">Remarks</span></span>

<span data-ttu-id="5a074-120">Ниже приведен пример связи, представленной объектом **иконтекстлинк** .</span><span class="sxs-lookup"><span data-stu-id="5a074-120">The following is an example of a relationship represented by an **IContextLink** object:</span></span>

-   <span data-ttu-id="5a074-121">При использовании узла Аналисишинт в анализе рукописного ввода операция анализа рукописного ввода создает объект **иконтекстлинк** типа аналисишинт между узлом подсказок по анализу и узлом, содержащим запись в области подсказки.</span><span class="sxs-lookup"><span data-stu-id="5a074-121">When an AnalysisHint node is used in ink analysis, the ink analysis operation creates an **IContextLink** object of type AnalysisHint between the analysis hint node and the node that contains writing within the area of the hint.</span></span> <span data-ttu-id="5a074-122">Исходный узел — это узел указания по анализу, а узел назначения — это узел, содержащий запись.</span><span class="sxs-lookup"><span data-stu-id="5a074-122">The source node is the analysis hint node and the destination node is the node that contains writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a074-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5a074-123">Requirements</span></span>



| <span data-ttu-id="5a074-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5a074-124">Requirement</span></span> | <span data-ttu-id="5a074-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5a074-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a074-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a074-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a074-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5a074-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5a074-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a074-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a074-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5a074-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5a074-130">Header</span><span class="sxs-lookup"><span data-stu-id="5a074-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a074-131"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5a074-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5a074-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5a074-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a074-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a074-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5a074-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a074-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a074-135">**Иконтекстноде:: Жетконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="5a074-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="5a074-136">**иконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="5a074-136">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="5a074-137">**контекстлинкдиректион**</span><span class="sxs-lookup"><span data-stu-id="5a074-137">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="5a074-138">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="5a074-138">Context Node Types</span></span>](context-node-types.md)
</dt> </dl>

 

