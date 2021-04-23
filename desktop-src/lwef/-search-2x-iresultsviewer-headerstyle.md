---
title: Свойство Хеадерстиле Иресултсвиевер (Вдсвиев. h)
description: Стиль заголовка, отображаемого в представлении.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Свойства Хеадерстиле устаревшие функции среды Windows
- Свойства Хеадерстиле устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство Хеадерстиле
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802345"
---
# <a name="iresultsviewerheaderstyle-property"></a><span data-ttu-id="853ce-106">Свойство Иресултсвиевер:: Хеадерстиле</span><span class="sxs-lookup"><span data-stu-id="853ce-106">IResultsViewer::HeaderStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="853ce-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="853ce-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="853ce-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="853ce-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="853ce-109">Стиль заголовка, отображаемого в представлении.</span><span class="sxs-lookup"><span data-stu-id="853ce-109">The style of header displayed in the view.</span></span>

<span data-ttu-id="853ce-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="853ce-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="853ce-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="853ce-111">Syntax</span></span>


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="853ce-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="853ce-112">Property value</span></span>

<span data-ttu-id="853ce-113">Задает стиль отображаемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="853ce-113">Sets the style of the header displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="853ce-114">Требования</span><span class="sxs-lookup"><span data-stu-id="853ce-114">Requirements</span></span>



| <span data-ttu-id="853ce-115">Требование</span><span class="sxs-lookup"><span data-stu-id="853ce-115">Requirement</span></span> | <span data-ttu-id="853ce-116">Значение</span><span class="sxs-lookup"><span data-stu-id="853ce-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="853ce-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="853ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="853ce-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="853ce-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="853ce-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="853ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="853ce-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="853ce-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="853ce-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="853ce-121">Redistributable</span></span><br/>          | <span data-ttu-id="853ce-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="853ce-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="853ce-123">Header</span><span class="sxs-lookup"><span data-stu-id="853ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="853ce-124"><dt>Вдсвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="853ce-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





