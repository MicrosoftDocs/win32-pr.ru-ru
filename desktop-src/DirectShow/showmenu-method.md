---
description: Метод Шовмену отображает указанное меню на экране.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Метод Шовмену
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806239"
---
# <a name="showmenu-method"></a><span data-ttu-id="619b9-103">Метод Шовмену</span><span class="sxs-lookup"><span data-stu-id="619b9-103">ShowMenu Method</span></span>

> [!Note]  
> <span data-ttu-id="619b9-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="619b9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="619b9-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="619b9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="619b9-106">`ShowMenu`Метод отображает указанное меню на экране.</span><span class="sxs-lookup"><span data-stu-id="619b9-106">The `ShowMenu` method displays the specified menu on the screen.</span></span>

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a><span data-ttu-id="619b9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="619b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="619b9-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*именуид*</span><span class="sxs-lookup"><span data-stu-id="619b9-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span></span>
</dt> <dd>

<span data-ttu-id="619b9-109">Указывает идентификатор меню в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="619b9-109">Specifies the menu ID as an Integer.</span></span>



| <span data-ttu-id="619b9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="619b9-110">Value</span></span> | <span data-ttu-id="619b9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="619b9-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="619b9-112">2</span><span class="sxs-lookup"><span data-stu-id="619b9-112">2</span></span>     | <span data-ttu-id="619b9-113">Заголовок (Top)</span><span class="sxs-lookup"><span data-stu-id="619b9-113">Title (Top)</span></span> |
| <span data-ttu-id="619b9-114">3</span><span class="sxs-lookup"><span data-stu-id="619b9-114">3</span></span>     | <span data-ttu-id="619b9-115">Root</span><span class="sxs-lookup"><span data-stu-id="619b9-115">Root</span></span>        |
| <span data-ttu-id="619b9-116">4</span><span class="sxs-lookup"><span data-stu-id="619b9-116">4</span></span>     | <span data-ttu-id="619b9-117">Субтитров</span><span class="sxs-lookup"><span data-stu-id="619b9-117">Subpicture</span></span>  |
| <span data-ttu-id="619b9-118">5</span><span class="sxs-lookup"><span data-stu-id="619b9-118">5</span></span>     | <span data-ttu-id="619b9-119">звук;</span><span class="sxs-lookup"><span data-stu-id="619b9-119">Audio</span></span>       |
| <span data-ttu-id="619b9-120">6</span><span class="sxs-lookup"><span data-stu-id="619b9-120">6</span></span>     | <span data-ttu-id="619b9-121">Angle</span><span class="sxs-lookup"><span data-stu-id="619b9-121">Angle</span></span>       |
| <span data-ttu-id="619b9-122">7</span><span class="sxs-lookup"><span data-stu-id="619b9-122">7</span></span>     | <span data-ttu-id="619b9-123">Глава</span><span class="sxs-lookup"><span data-stu-id="619b9-123">Chapter</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="619b9-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="619b9-124">Return Value</span></span>

<span data-ttu-id="619b9-125">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="619b9-125">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="619b9-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="619b9-126">Remarks</span></span>

<span data-ttu-id="619b9-127">Имена меню DVD могут быть несколько запутанными.</span><span class="sxs-lookup"><span data-stu-id="619b9-127">DVD menu names can be somewhat confusing.</span></span> <span data-ttu-id="619b9-128">Меню заголовок — это еще одно имя для меню менеджер видео — главное меню для всего диска. обычно в нем перечислены все наборы заголовков видео, доступные на диске. Корневое меню — это меню для одного набора заголовков видео, которое может содержать один заголовок или группу заголовков.</span><span class="sxs-lookup"><span data-stu-id="619b9-128">The title menu is another name for the Video Manager Menu, the main menu for the entire disc; it generally lists all the video title sets available on the disc. The root menu is the menu for one video title set, which can contain one title or a group of titles.</span></span> <span data-ttu-id="619b9-129">Все заголовки в наборе заголовков имеют одинаковые меню "подизображение", "звук" и "угол".</span><span class="sxs-lookup"><span data-stu-id="619b9-129">All the titles in a title set share the same Subpicture, Audio, and Angle menus.</span></span>

 

 



