---
title: Свойство Индексколумн Иресултпроперти (Вдсшаредидл. h)
description: Имя столбца свойств в индексе.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Свойства Индексколумн устаревшие функции среды Windows
- Свойства Индексколумн устаревшие функции среды Windows, интерфейс Иресултпроперти
- Интерфейс Иресултпроперти устаревшие функции среды Windows, свойство Индексколумн
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891729"
---
# <a name="iresultpropertyindexcolumn-property"></a><span data-ttu-id="631b9-106">Свойство Иресултпроперти:: Индексколумн</span><span class="sxs-lookup"><span data-stu-id="631b9-106">IResultProperty::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="631b9-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="631b9-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="631b9-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="631b9-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="631b9-109">Имя столбца свойств в индексе.</span><span class="sxs-lookup"><span data-stu-id="631b9-109">Properties column name in the index.</span></span>

<span data-ttu-id="631b9-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="631b9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="631b9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="631b9-111">Syntax</span></span>


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="631b9-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="631b9-112">Property value</span></span>

<span data-ttu-id="631b9-113">Возвращает указатель на имя столбца в индексе.</span><span class="sxs-lookup"><span data-stu-id="631b9-113">returns a pointer to the column name in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="631b9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="631b9-114">Requirements</span></span>



| <span data-ttu-id="631b9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="631b9-115">Requirement</span></span> | <span data-ttu-id="631b9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="631b9-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="631b9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="631b9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="631b9-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="631b9-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="631b9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="631b9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="631b9-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="631b9-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="631b9-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="631b9-121">Redistributable</span></span><br/>          | <span data-ttu-id="631b9-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="631b9-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="631b9-123">Header</span><span class="sxs-lookup"><span data-stu-id="631b9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="631b9-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="631b9-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





