---
title: Свойство QueryText Иресултсвиевер (Вдсвиев. h)
description: Возвращает или задает текст текущего запроса.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Свойства QueryText устаревшие функции среды Windows
- Свойства QueryText устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство QueryText
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98450114ad64ec0209b14041b8f2516dc6884b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137299"
---
# <a name="iresultsviewerquerytext-property"></a><span data-ttu-id="041c0-106">Свойство Иресултсвиевер:: QueryText</span><span class="sxs-lookup"><span data-stu-id="041c0-106">IResultsViewer::QueryText property</span></span>

> [!NOTE]
> <span data-ttu-id="041c0-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="041c0-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="041c0-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="041c0-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="041c0-109">Возвращает или задает текст текущего запроса.</span><span class="sxs-lookup"><span data-stu-id="041c0-109">Gets or sets the current query text.</span></span>

<span data-ttu-id="041c0-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="041c0-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="041c0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="041c0-111">Syntax</span></span>


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a><span data-ttu-id="041c0-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="041c0-112">Property value</span></span>

<span data-ttu-id="041c0-113">Задает текст текущего запроса.</span><span class="sxs-lookup"><span data-stu-id="041c0-113">Sets the current query text.</span></span>

## <a name="requirements"></a><span data-ttu-id="041c0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="041c0-114">Requirements</span></span>



| <span data-ttu-id="041c0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="041c0-115">Requirement</span></span> | <span data-ttu-id="041c0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="041c0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="041c0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="041c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="041c0-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="041c0-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="041c0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="041c0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="041c0-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="041c0-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="041c0-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="041c0-121">Redistributable</span></span><br/>          | <span data-ttu-id="041c0-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="041c0-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="041c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="041c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="041c0-124"><dt>Вдсвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="041c0-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





