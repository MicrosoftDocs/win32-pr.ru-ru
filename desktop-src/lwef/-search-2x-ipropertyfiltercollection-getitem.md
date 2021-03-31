---
title: Свойство Ипропертифилтерколлектион-ITem (Вдсшаредидл. h)
description: Возвращает конкретный фильтр в коллекции.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Свойство DataItem устаревшие функции среды Windows
- Свойство DataItem устаревшие функции среды Windows, интерфейс Ипропертифилтерколлектион
- Интерфейс Ипропертифилтерколлектион устаревшие функции среды Windows, свойство DataItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988504"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a><span data-ttu-id="8fbf4-106">Свойство Ипропертифилтерколлектион:: ITem</span><span class="sxs-lookup"><span data-stu-id="8fbf4-106">IPropertyFilterCollection::GetITem property</span></span>

> [!NOTE]
> <span data-ttu-id="8fbf4-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8fbf4-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8fbf4-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8fbf4-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8fbf4-109">Возвращает конкретный фильтр в коллекции.</span><span class="sxs-lookup"><span data-stu-id="8fbf4-109">Returns a specific filter within the collection.</span></span>

<span data-ttu-id="8fbf4-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8fbf4-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbf4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fbf4-111">Syntax</span></span>


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="8fbf4-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8fbf4-112">Property value</span></span>

<span data-ttu-id="8fbf4-113">Задает адрес фильтра.</span><span class="sxs-lookup"><span data-stu-id="8fbf4-113">Sets the address of the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fbf4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8fbf4-114">Requirements</span></span>



| <span data-ttu-id="8fbf4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8fbf4-115">Requirement</span></span> | <span data-ttu-id="8fbf4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbf4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbf4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fbf4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbf4-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fbf4-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8fbf4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fbf4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbf4-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fbf4-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8fbf4-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8fbf4-121">Redistributable</span></span><br/>          | <span data-ttu-id="8fbf4-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8fbf4-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="8fbf4-123">Header</span><span class="sxs-lookup"><span data-stu-id="8fbf4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fbf4-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fbf4-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





