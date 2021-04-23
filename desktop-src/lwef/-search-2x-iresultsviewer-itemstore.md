---
title: Свойство ItemStore Иресултсвиевер (Вдсвиев. h)
description: Это свойство задает или возвращает имя хранилища, по которому будут фильтроваться результаты.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- Свойства ItemStore устаревшие функции среды Windows
- Свойства ItemStore устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство ItemStore
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99abd4ef7ee36a0c76efa391d98a9fdb1d75f34e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490398"
---
# <a name="iresultsvieweritemstore-property"></a><span data-ttu-id="917bb-106">Свойство Иресултсвиевер:: ItemStore</span><span class="sxs-lookup"><span data-stu-id="917bb-106">IResultsViewer::ItemStore property</span></span>

> [!NOTE]
> <span data-ttu-id="917bb-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="917bb-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="917bb-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="917bb-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="917bb-109">Это свойство задает или возвращает имя хранилища, по которому будут фильтроваться результаты.</span><span class="sxs-lookup"><span data-stu-id="917bb-109">This property will set or return the name of the store to filter results by.</span></span>

<span data-ttu-id="917bb-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="917bb-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="917bb-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="917bb-111">Syntax</span></span>


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="917bb-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="917bb-112">Property value</span></span>

<span data-ttu-id="917bb-113">Задает имена хранилища.</span><span class="sxs-lookup"><span data-stu-id="917bb-113">Sets the names of the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="917bb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="917bb-114">Requirements</span></span>



| <span data-ttu-id="917bb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="917bb-115">Requirement</span></span> | <span data-ttu-id="917bb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="917bb-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="917bb-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="917bb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="917bb-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="917bb-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="917bb-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="917bb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="917bb-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="917bb-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="917bb-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="917bb-121">Redistributable</span></span><br/>          | <span data-ttu-id="917bb-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="917bb-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="917bb-123">Header</span><span class="sxs-lookup"><span data-stu-id="917bb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="917bb-124"><dt>Вдсвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="917bb-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





