---
title: Перечисление Виевконтентс
description: Используется по содержимому Иресултсвиевер для указания или установки способа отображения текущего набора возвращаемых данных запроса.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Перечисление Виевконтентс. устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699234"
---
# <a name="viewcontents-enumeration"></a><span data-ttu-id="08187-104">Перечисление Виевконтентс</span><span class="sxs-lookup"><span data-stu-id="08187-104">ViewContents enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="08187-105">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="08187-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="08187-106">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="08187-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="08187-107">Используется [**иресултсвиевер:: Content**](-search-2x-iresultsviewer-contents.md) , чтобы указать или задать способ отображения текущего набора возвращаемых данных запроса.</span><span class="sxs-lookup"><span data-stu-id="08187-107">Used by [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) to indicate or set how the current query return set is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="08187-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08187-108">Syntax</span></span>


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a><span data-ttu-id="08187-109">Константы</span><span class="sxs-lookup"><span data-stu-id="08187-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="08187-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ресултсдисплайед**</span><span class="sxs-lookup"><span data-stu-id="08187-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="08187-111">Указывает тип содержимого, отображаемого в представлении результатов.</span><span class="sxs-lookup"><span data-stu-id="08187-111">Indicates the type of contents being displayed in the results view.</span></span>

</dd> <dt>

<span data-ttu-id="08187-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**шеллвиевдисплайед**</span><span class="sxs-lookup"><span data-stu-id="08187-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="08187-113">Указывает, что тип содержимого, отображаемого в представлении результатов, в настоящее время установлен на представление оболочки.</span><span class="sxs-lookup"><span data-stu-id="08187-113">Indicates the type of contents being displayed in the results view is currently set to the Shell view.</span></span>

</dd> <dt>

<span data-ttu-id="08187-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**веббровсердисплайед**</span><span class="sxs-lookup"><span data-stu-id="08187-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="08187-115">Указывает, что тип содержимого, отображаемого в представлении результатов, в настоящее время установлен в представление браузера.</span><span class="sxs-lookup"><span data-stu-id="08187-115">Indicates the type of contents being displayed in the results view is currently set to the browser view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08187-116">Требования</span><span class="sxs-lookup"><span data-stu-id="08187-116">Requirements</span></span>



| <span data-ttu-id="08187-117">Требование</span><span class="sxs-lookup"><span data-stu-id="08187-117">Requirement</span></span> | <span data-ttu-id="08187-118">Значение</span><span class="sxs-lookup"><span data-stu-id="08187-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08187-119">IDL</span><span class="sxs-lookup"><span data-stu-id="08187-119">IDL</span></span><br/> | <dl> <span data-ttu-id="08187-120"><dt>Вдсвиев. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08187-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





