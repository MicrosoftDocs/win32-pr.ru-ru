---
title: Свойство SortProperty Иресултсвиевер (Вдсвиев. h)
description: Это свойство задаст или возвратит Индексколумн свойства для сортировки результатов по.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Свойства SortProperty устаревшие функции среды Windows
- Свойства SortProperty устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство SortProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891857"
---
# <a name="iresultsviewersortproperty-property"></a><span data-ttu-id="05b4a-106">Свойство Иресултсвиевер:: SortProperty</span><span class="sxs-lookup"><span data-stu-id="05b4a-106">IResultsViewer::SortProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="05b4a-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="05b4a-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="05b4a-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="05b4a-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="05b4a-109">Это свойство задаст или возвратит Индексколумн свойства для сортировки результатов по.</span><span class="sxs-lookup"><span data-stu-id="05b4a-109">This property will set or return the IndexColumn of the property to sort results by.</span></span>

<span data-ttu-id="05b4a-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="05b4a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b4a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05b4a-111">Syntax</span></span>


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="05b4a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="05b4a-112">Property value</span></span>

<span data-ttu-id="05b4a-113">Задает свойство Индексколумн.</span><span class="sxs-lookup"><span data-stu-id="05b4a-113">Sets the IndexColumn property.</span></span>

## <a name="requirements"></a><span data-ttu-id="05b4a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="05b4a-114">Requirements</span></span>



| <span data-ttu-id="05b4a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="05b4a-115">Requirement</span></span> | <span data-ttu-id="05b4a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="05b4a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="05b4a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05b4a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="05b4a-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="05b4a-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="05b4a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05b4a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="05b4a-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="05b4a-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="05b4a-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="05b4a-121">Redistributable</span></span><br/>          | <span data-ttu-id="05b4a-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="05b4a-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="05b4a-123">Header</span><span class="sxs-lookup"><span data-stu-id="05b4a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="05b4a-124"><dt>Вдсвиев. h</dt></span><span class="sxs-lookup"><span data-stu-id="05b4a-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





