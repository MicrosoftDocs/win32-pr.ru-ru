---
title: Свойство FilterType Иресултсвиевер (Вдсвиев. h)
description: Это свойство задает или возвращает имя типа прецеивед, по которому будут фильтроваться результаты.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- Свойства FilterType устаревшие функции среды Windows
- Свойства FilterType устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство FilterType
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890d0ceadddb9f3b46ee8b45f109a389472be218
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691956"
---
# <a name="iresultsviewerfiltertype-property"></a><span data-ttu-id="6907d-106">Свойство Иресултсвиевер:: FilterType</span><span class="sxs-lookup"><span data-stu-id="6907d-106">IResultsViewer::FilterType property</span></span>

> [!NOTE]
> <span data-ttu-id="6907d-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6907d-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6907d-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="6907d-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6907d-109">Это свойство задает или возвращает имя типа прецеивед, по которому будут фильтроваться результаты.</span><span class="sxs-lookup"><span data-stu-id="6907d-109">This property will set or return the name of the preceived type to filter results by.</span></span>

<span data-ttu-id="6907d-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6907d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6907d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6907d-111">Syntax</span></span>


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="6907d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6907d-112">Property value</span></span>

<span data-ttu-id="6907d-113">Задает воспринимаемый тип, используемый для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="6907d-113">Sets the perceived type used to filter results.</span></span>

## <a name="requirements"></a><span data-ttu-id="6907d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6907d-114">Requirements</span></span>



| <span data-ttu-id="6907d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6907d-115">Requirement</span></span> | <span data-ttu-id="6907d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6907d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6907d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6907d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6907d-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6907d-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6907d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6907d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6907d-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="6907d-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="6907d-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6907d-121">Redistributable</span></span><br/>          | <span data-ttu-id="6907d-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="6907d-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="6907d-123">Header</span><span class="sxs-lookup"><span data-stu-id="6907d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6907d-124"><dt>Вдсвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="6907d-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





