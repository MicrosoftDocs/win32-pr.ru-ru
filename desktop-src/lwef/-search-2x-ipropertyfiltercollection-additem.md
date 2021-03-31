---
title: Свойство AddItem Ипропертифилтерколлектион (Вдсшаредидл. h)
description: Добавляет новый фильтр в коллекцию.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- Свойства AddItem устаревшие функции среды Windows
- Свойство AddItem устаревшие функции среды Windows, интерфейс Ипропертифилтерколлектион
- Интерфейс Ипропертифилтерколлектион устаревшие функции среды Windows, свойство AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071480"
---
# <a name="ipropertyfiltercollectionadditem-property"></a><span data-ttu-id="c0df9-106">Свойство Ипропертифилтерколлектион:: AddItem</span><span class="sxs-lookup"><span data-stu-id="c0df9-106">IPropertyFilterCollection::AddItem property</span></span>

> [!NOTE]
> <span data-ttu-id="c0df9-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c0df9-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c0df9-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c0df9-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c0df9-109">Добавляет новый фильтр в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="c0df9-109">Adds a new filter to the collection.</span></span>

<span data-ttu-id="c0df9-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c0df9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0df9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0df9-111">Syntax</span></span>


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="c0df9-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c0df9-112">Property value</span></span>

<span data-ttu-id="c0df9-113">Возвращает указатель на адрес для нового фильтра.</span><span class="sxs-lookup"><span data-stu-id="c0df9-113">returns a pointer to the address for the new filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0df9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c0df9-114">Requirements</span></span>



| <span data-ttu-id="c0df9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c0df9-115">Requirement</span></span> | <span data-ttu-id="c0df9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c0df9-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0df9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0df9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0df9-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0df9-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c0df9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0df9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0df9-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0df9-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c0df9-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c0df9-121">Redistributable</span></span><br/>          | <span data-ttu-id="c0df9-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="c0df9-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="c0df9-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0df9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0df9-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0df9-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





