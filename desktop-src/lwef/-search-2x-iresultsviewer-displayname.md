---
title: Свойство DisplayName Иресултсвиевер (Вдсвиев. h)
description: Локализованное отображаемое имя типа.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- Свойства DisplayName устаревшие функции среды Windows
- Свойства DisplayName устаревшие компоненты среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство DisplayName
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5ba65729fb238dbed57b71d893a9814c8ac8f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691820"
---
# <a name="iresultsviewerdisplayname-property"></a><span data-ttu-id="56773-106">Иресултсвиевер: свойство Исплайнаме:D</span><span class="sxs-lookup"><span data-stu-id="56773-106">IResultsViewer::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="56773-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56773-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="56773-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="56773-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="56773-109">Локализованное отображаемое имя типа.</span><span class="sxs-lookup"><span data-stu-id="56773-109">Localized display name of the type.</span></span>

<span data-ttu-id="56773-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="56773-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56773-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56773-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="56773-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="56773-112">Property value</span></span>

<span data-ttu-id="56773-113">Указатель на значение, получающее локализованное отображаемое имя для типа.</span><span class="sxs-lookup"><span data-stu-id="56773-113">Pointer to a value that receives the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="56773-114">Требования</span><span class="sxs-lookup"><span data-stu-id="56773-114">Requirements</span></span>



| <span data-ttu-id="56773-115">Требование</span><span class="sxs-lookup"><span data-stu-id="56773-115">Requirement</span></span> | <span data-ttu-id="56773-116">Значение</span><span class="sxs-lookup"><span data-stu-id="56773-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="56773-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56773-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56773-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="56773-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="56773-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56773-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56773-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="56773-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="56773-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="56773-121">Redistributable</span></span><br/>          | <span data-ttu-id="56773-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="56773-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="56773-123">Header</span><span class="sxs-lookup"><span data-stu-id="56773-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="56773-124"><dt>Вдсвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="56773-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





