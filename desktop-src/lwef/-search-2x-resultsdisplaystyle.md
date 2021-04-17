---
title: Перечисление Ресултсдисплайстиле
description: Используется Иресултсвиевер Ресултсстиле для установки или определения способа отображения результатов.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- Перечисление Ресултсдисплайстиле. устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698976"
---
# <a name="resultsdisplaystyle-enumeration"></a><span data-ttu-id="856bb-104">Перечисление Ресултсдисплайстиле</span><span class="sxs-lookup"><span data-stu-id="856bb-104">ResultsDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="856bb-105">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="856bb-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="856bb-106">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="856bb-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="856bb-107">Используется [**иресултсвиевер:: ресултсстиле**](-search-2x-iresultsviewer-resultsstyle.md) для задания или определения способа отображения результатов.</span><span class="sxs-lookup"><span data-stu-id="856bb-107">Used by [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) to set or determine how results are displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="856bb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="856bb-108">Syntax</span></span>


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="856bb-109">Константы</span><span class="sxs-lookup"><span data-stu-id="856bb-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="856bb-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**смалликонресултс**</span><span class="sxs-lookup"><span data-stu-id="856bb-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="856bb-111">Показывает, что результаты отображаются в виде мелких значков.</span><span class="sxs-lookup"><span data-stu-id="856bb-111">Indicates Results are displayed as small icons.</span></span>

</dd> <dt>

<span data-ttu-id="856bb-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**ларжеиконресултс**</span><span class="sxs-lookup"><span data-stu-id="856bb-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="856bb-113">Показывает, что результаты отображаются в виде крупных значков.</span><span class="sxs-lookup"><span data-stu-id="856bb-113">Indicates Results are displayed as large icons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="856bb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="856bb-114">Requirements</span></span>



| <span data-ttu-id="856bb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="856bb-115">Requirement</span></span> | <span data-ttu-id="856bb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="856bb-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="856bb-117">IDL</span><span class="sxs-lookup"><span data-stu-id="856bb-117">IDL</span></span><br/> | <dl> <span data-ttu-id="856bb-118"><dt>Вдсвиев. idl</dt></span><span class="sxs-lookup"><span data-stu-id="856bb-118"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





