---
title: Свойство Ипропертифилтерколлектион Count (Вдсшаредидл. h)
description: Число фильтров в коллекции.
ms.assetid: 9d656f06-eb1d-4cc6-9096-252f0fc65ae2
keywords:
- Свойство Count устаревшие функции среды Windows
- Свойство Count устаревшие функции среды Windows, интерфейс Ипропертифилтерколлектион
- Интерфейс Ипропертифилтерколлектион устаревшие функции среды Windows, свойство Count
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.Count
- IPropertyFilterCollection.get_Count
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258a2ca8089cecb8e2e15fbe7e9e92ce1ed3468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801936"
---
# <a name="ipropertyfiltercollectioncount-property"></a><span data-ttu-id="61618-106">Свойство Ипропертифилтерколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="61618-106">IPropertyFilterCollection::Count property</span></span>

> [!NOTE]
> <span data-ttu-id="61618-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="61618-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="61618-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="61618-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="61618-109">Число фильтров в коллекции.</span><span class="sxs-lookup"><span data-stu-id="61618-109">Number of filters in the collection.</span></span>

<span data-ttu-id="61618-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="61618-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61618-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61618-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="61618-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="61618-112">Property value</span></span>

<span data-ttu-id="61618-113">Возвращает указатель на число фильтров в коллекции.</span><span class="sxs-lookup"><span data-stu-id="61618-113">returns a pointer to the number of filters in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="61618-114">Требования</span><span class="sxs-lookup"><span data-stu-id="61618-114">Requirements</span></span>



| <span data-ttu-id="61618-115">Требование</span><span class="sxs-lookup"><span data-stu-id="61618-115">Requirement</span></span> | <span data-ttu-id="61618-116">Значение</span><span class="sxs-lookup"><span data-stu-id="61618-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="61618-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61618-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61618-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="61618-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="61618-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61618-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61618-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="61618-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="61618-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="61618-121">Redistributable</span></span><br/>          | <span data-ttu-id="61618-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="61618-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="61618-123">Header</span><span class="sxs-lookup"><span data-stu-id="61618-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="61618-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="61618-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





