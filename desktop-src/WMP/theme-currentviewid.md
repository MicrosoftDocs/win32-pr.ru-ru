---
title: THEME. Куррентвиевид
description: Атрибут Куррентвиевид указывает или получает отображаемое в данный момент представление.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- Проигрыватель Windows Media THEME. Куррентвиевид
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648769"
---
# <a name="themecurrentviewid"></a><span data-ttu-id="a3dc8-104">THEME. Куррентвиевид</span><span class="sxs-lookup"><span data-stu-id="a3dc8-104">THEME.currentViewID</span></span>

<span data-ttu-id="a3dc8-105">Атрибут **куррентвиевид** указывает или получает отображаемое в данный момент **представление**.</span><span class="sxs-lookup"><span data-stu-id="a3dc8-105">The **currentViewID** attribute specifies or retrieves the currently displayed **VIEW**.</span></span>

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a><span data-ttu-id="a3dc8-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a3dc8-106">Possible Values</span></span>

<span data-ttu-id="a3dc8-107">Этот атрибут является **строкой** для чтения и записи, указывающей **идентификатор** текущего **представления**.</span><span class="sxs-lookup"><span data-stu-id="a3dc8-107">This attribute is a read/write **String** specifying the **id** of the current **VIEW**.</span></span> <span data-ttu-id="a3dc8-108">У него нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3dc8-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3dc8-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3dc8-109">Remarks</span></span>

<span data-ttu-id="a3dc8-110">При указании **куррентвиевид** автоматически закрывается существующий **куррентвиев** (на который указывает глобальный атрибут **представления** ) и открывается указанное **представление**.</span><span class="sxs-lookup"><span data-stu-id="a3dc8-110">Specifying **currentViewID** automatically closes the existing **currentView** (pointed to by the **view** global attribute) and opens the specified **VIEW**.</span></span>

## <a name="examples"></a><span data-ttu-id="a3dc8-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="a3dc8-111">Examples</span></span>


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="a3dc8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a3dc8-112">Requirements</span></span>



| <span data-ttu-id="a3dc8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a3dc8-113">Requirement</span></span> | <span data-ttu-id="a3dc8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a3dc8-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a3dc8-115">Версия</span><span class="sxs-lookup"><span data-stu-id="a3dc8-115">Version</span></span><br/> | <span data-ttu-id="a3dc8-116">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="a3dc8-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3dc8-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3dc8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3dc8-118">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="a3dc8-118">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





