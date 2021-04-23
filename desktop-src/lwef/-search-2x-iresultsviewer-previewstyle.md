---
title: Свойство Превиевстиле Иресултсвиевер (Вдсвиев. h)
description: Управляет режимом просмотра панели просмотра.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- Свойства Превиевстиле устаревшие функции среды Windows
- Свойства Превиевстиле устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство Превиевстиле
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb3cb2cfd94d5cf1e93080259257bb27fa4f086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710447"
---
# <a name="iresultsviewerpreviewstyle-property"></a><span data-ttu-id="595a4-106">Иресултсвиевер: свойство Ревиевстиле:P</span><span class="sxs-lookup"><span data-stu-id="595a4-106">IResultsViewer::PreviewStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="595a4-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="595a4-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="595a4-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="595a4-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="595a4-109">Управляет режимом просмотра панели просмотра.</span><span class="sxs-lookup"><span data-stu-id="595a4-109">Controls the preview pane's display mode.</span></span>

<span data-ttu-id="595a4-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="595a4-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="595a4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="595a4-111">Syntax</span></span>


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="595a4-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="595a4-112">Property value</span></span>

<span data-ttu-id="595a4-113">Задает текущее свойство стиля для панели предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="595a4-113">Sets the current style property for the preview pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="595a4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="595a4-114">Requirements</span></span>



| <span data-ttu-id="595a4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="595a4-115">Requirement</span></span> | <span data-ttu-id="595a4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="595a4-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="595a4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="595a4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="595a4-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="595a4-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="595a4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="595a4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="595a4-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="595a4-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="595a4-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="595a4-121">Redistributable</span></span><br/>          | <span data-ttu-id="595a4-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="595a4-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="595a4-123">Header</span><span class="sxs-lookup"><span data-stu-id="595a4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="595a4-124"><dt>Вдсвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="595a4-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





