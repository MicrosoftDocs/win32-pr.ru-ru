---
title: Свойство RemoveItem Ипропертифилтерколлектион (Вдсшаредидл. h)
description: Удаляет конкретный фильтр в коллекции.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- Свойства RemoveItem устаревшие функции среды Windows
- Свойства RemoveItem устаревшие функции среды Windows, интерфейс Ипропертифилтерколлектион
- Интерфейс Ипропертифилтерколлектион устаревшие функции среды Windows, свойство RemoveItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802896"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a><span data-ttu-id="79fed-106">Свойство Ипропертифилтерколлектион:: RemoveItem</span><span class="sxs-lookup"><span data-stu-id="79fed-106">IPropertyFilterCollection::RemoveItem property</span></span>

> [!NOTE]
> <span data-ttu-id="79fed-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79fed-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="79fed-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="79fed-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="79fed-109">Удаляет конкретный фильтр в коллекции.</span><span class="sxs-lookup"><span data-stu-id="79fed-109">Removes a specific filter to the collection.</span></span>

<span data-ttu-id="79fed-110">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="79fed-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79fed-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79fed-111">Syntax</span></span>


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a><span data-ttu-id="79fed-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="79fed-112">Property value</span></span>

<span data-ttu-id="79fed-113">Принимает указатель на индекс удаляемого фильтра.</span><span class="sxs-lookup"><span data-stu-id="79fed-113">Accepts a pointer to the index for the filter to be removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="79fed-114">Требования</span><span class="sxs-lookup"><span data-stu-id="79fed-114">Requirements</span></span>



| <span data-ttu-id="79fed-115">Требование</span><span class="sxs-lookup"><span data-stu-id="79fed-115">Requirement</span></span> | <span data-ttu-id="79fed-116">Значение</span><span class="sxs-lookup"><span data-stu-id="79fed-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="79fed-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79fed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79fed-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="79fed-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="79fed-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79fed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79fed-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="79fed-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="79fed-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="79fed-121">Redistributable</span></span><br/>          | <span data-ttu-id="79fed-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="79fed-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="79fed-123">Header</span><span class="sxs-lookup"><span data-stu-id="79fed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="79fed-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="79fed-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





