---
title: Перечисление Превиевдисплайстиле
description: Используется Иресултсвиевер Превиевстиле для установки или определения используемого в настоящий момент стиля дисплея.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- Перечисление Превиевдисплайстиле. устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699136"
---
# <a name="previewdisplaystyle-enumeration"></a><span data-ttu-id="1b78f-104">Перечисление Превиевдисплайстиле</span><span class="sxs-lookup"><span data-stu-id="1b78f-104">PreviewDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="1b78f-105">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1b78f-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="1b78f-106">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="1b78f-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="1b78f-107">Используется [**иресултсвиевер::P ревиевстиле**](-search-2x-iresultsviewer-previewstyle.md) , чтобы задать или определить используемый в настоящее время стиль дисплея.</span><span class="sxs-lookup"><span data-stu-id="1b78f-107">Used by [**IResultsViewer::PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md) to set or determine the display style currently being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b78f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b78f-108">Syntax</span></span>


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="1b78f-109">Константы</span><span class="sxs-lookup"><span data-stu-id="1b78f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1b78f-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**Автопросмотр**</span><span class="sxs-lookup"><span data-stu-id="1b78f-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**AutoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="1b78f-111">Указывает на Автопросмотр.</span><span class="sxs-lookup"><span data-stu-id="1b78f-111">Indicates AutoPreview.</span></span>

</dd> <dt>

<span data-ttu-id="1b78f-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**ригхтпревиев**</span><span class="sxs-lookup"><span data-stu-id="1b78f-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**</span></span>
</dt> <dd>

<span data-ttu-id="1b78f-113">Указывает Ригхтпревиев.</span><span class="sxs-lookup"><span data-stu-id="1b78f-113">Indicates RightPreview.</span></span>

</dd> <dt>

<span data-ttu-id="1b78f-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**боттомпревиев**</span><span class="sxs-lookup"><span data-stu-id="1b78f-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**</span></span>
</dt> <dd>

<span data-ttu-id="1b78f-115">Указывает Боттомпревиев.</span><span class="sxs-lookup"><span data-stu-id="1b78f-115">Indicates BottomPreview.</span></span>

</dd> <dt>

<span data-ttu-id="1b78f-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Непредварительная версия**</span><span class="sxs-lookup"><span data-stu-id="1b78f-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="1b78f-117">Указывает на непредварительную версию.</span><span class="sxs-lookup"><span data-stu-id="1b78f-117">Indicates NoPreview.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b78f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1b78f-118">Requirements</span></span>



| <span data-ttu-id="1b78f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1b78f-119">Requirement</span></span> | <span data-ttu-id="1b78f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1b78f-120">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b78f-121">IDL</span><span class="sxs-lookup"><span data-stu-id="1b78f-121">IDL</span></span><br/> | <dl> <span data-ttu-id="1b78f-122"><dt>Вдсвиев. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b78f-122"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





