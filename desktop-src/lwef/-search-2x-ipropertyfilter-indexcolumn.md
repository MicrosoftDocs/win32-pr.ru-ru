---
title: Свойство Индексколумн Ипропертифилтер (Вдсшаредидл. h)
description: Имя индексируемого столбца свойства, по которому производится фильтрация.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Свойства Индексколумн устаревшие функции среды Windows
- Свойства Индексколумн устаревшие функции среды Windows, интерфейс Ипропертифилтер
- Интерфейс Ипропертифилтер устаревшие функции среды Windows, свойство Индексколумн
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071574"
---
# <a name="ipropertyfilterindexcolumn-property"></a><span data-ttu-id="a26ce-106">Свойство Ипропертифилтер:: Индексколумн</span><span class="sxs-lookup"><span data-stu-id="a26ce-106">IPropertyFilter::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="a26ce-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a26ce-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a26ce-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="a26ce-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a26ce-109">Имя индексируемого столбца свойства, по которому производится фильтрация.</span><span class="sxs-lookup"><span data-stu-id="a26ce-109">Indexed column name of the property to filter by.</span></span>

<span data-ttu-id="a26ce-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a26ce-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a26ce-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a26ce-111">Syntax</span></span>


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="a26ce-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a26ce-112">Property value</span></span>

<span data-ttu-id="a26ce-113">Задает свойство Column.</span><span class="sxs-lookup"><span data-stu-id="a26ce-113">Sets the Column property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a26ce-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a26ce-114">Requirements</span></span>



| <span data-ttu-id="a26ce-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a26ce-115">Requirement</span></span> | <span data-ttu-id="a26ce-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a26ce-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a26ce-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a26ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a26ce-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a26ce-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a26ce-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a26ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a26ce-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="a26ce-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a26ce-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a26ce-121">Redistributable</span></span><br/>          | <span data-ttu-id="a26ce-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="a26ce-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="a26ce-123">Header</span><span class="sxs-lookup"><span data-stu-id="a26ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a26ce-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a26ce-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





