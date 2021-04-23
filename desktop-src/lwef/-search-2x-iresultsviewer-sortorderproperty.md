---
title: Свойство SortOrderProperty IResultsViewer (WdsView.h)
description: Это свойство задает или возвращает порядок столбцов для сортировки результатов по.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Свойства Сортордерпроперти устаревшие функции среды Windows
- Свойства Сортордерпроперти устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство Сортордерпроперти
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672649"
---
# <a name="iresultsviewersortorderproperty-property"></a><span data-ttu-id="13a39-106">Свойство Иресултсвиевер:: Сортордерпроперти</span><span class="sxs-lookup"><span data-stu-id="13a39-106">IResultsViewer::SortOrderProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="13a39-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="13a39-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="13a39-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="13a39-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="13a39-109">Это свойство задает или возвращает порядок столбцов для сортировки результатов по.</span><span class="sxs-lookup"><span data-stu-id="13a39-109">This property will set or return the order of columns to sort results by.</span></span>

<span data-ttu-id="13a39-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="13a39-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a39-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13a39-111">Syntax</span></span>


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a><span data-ttu-id="13a39-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="13a39-112">Property value</span></span>

<span data-ttu-id="13a39-113">Задает свойство [**колумнсортордер**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) .</span><span class="sxs-lookup"><span data-stu-id="13a39-113">Sets the [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a39-114">Требования</span><span class="sxs-lookup"><span data-stu-id="13a39-114">Requirements</span></span>



| <span data-ttu-id="13a39-115">Требование</span><span class="sxs-lookup"><span data-stu-id="13a39-115">Requirement</span></span> | <span data-ttu-id="13a39-116">Значение</span><span class="sxs-lookup"><span data-stu-id="13a39-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="13a39-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13a39-117">Minimum supported client</span></span><br/> | <span data-ttu-id="13a39-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="13a39-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="13a39-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13a39-119">Minimum supported server</span></span><br/> | <span data-ttu-id="13a39-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="13a39-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="13a39-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="13a39-121">Redistributable</span></span><br/>          | <span data-ttu-id="13a39-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="13a39-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="13a39-123">Header</span><span class="sxs-lookup"><span data-stu-id="13a39-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a39-124"><dt>Вдсвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="13a39-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





