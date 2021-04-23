---
description: Событие Шовмену отправляется, когда диск включает или отключает отображение меню.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: шовмену
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990148"
---
# <a name="showmenu"></a><span data-ttu-id="caf4e-103">шовмену</span><span class="sxs-lookup"><span data-stu-id="caf4e-103">ShowMenu</span></span>

> [!Note]  
> <span data-ttu-id="caf4e-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="caf4e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="caf4e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="caf4e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="caf4e-106">`ShowMenu`Событие отправляется, когда диск включает или отключает отображение меню.</span><span class="sxs-lookup"><span data-stu-id="caf4e-106">The `ShowMenu` event is sent when the disc enables or disables the showing of a menu.</span></span>

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a><span data-ttu-id="caf4e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="caf4e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf4e-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*двдменуидконстантс*</span><span class="sxs-lookup"><span data-stu-id="caf4e-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span></span>
</dt> <dd>

<span data-ttu-id="caf4e-109">Указывает, какое меню было включено или отключено в качестве числового значения.</span><span class="sxs-lookup"><span data-stu-id="caf4e-109">Specifies which menu has been enabled or disabled as a Number value.</span></span>



| <span data-ttu-id="caf4e-110">Значение</span><span class="sxs-lookup"><span data-stu-id="caf4e-110">Value</span></span> | <span data-ttu-id="caf4e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="caf4e-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="caf4e-112">2</span><span class="sxs-lookup"><span data-stu-id="caf4e-112">2</span></span>     | <span data-ttu-id="caf4e-113">Название</span><span class="sxs-lookup"><span data-stu-id="caf4e-113">Title</span></span>       |
| <span data-ttu-id="caf4e-114">3</span><span class="sxs-lookup"><span data-stu-id="caf4e-114">3</span></span>     | <span data-ttu-id="caf4e-115">Root</span><span class="sxs-lookup"><span data-stu-id="caf4e-115">Root</span></span>        |
| <span data-ttu-id="caf4e-116">4</span><span class="sxs-lookup"><span data-stu-id="caf4e-116">4</span></span>     | <span data-ttu-id="caf4e-117">Субтитров</span><span class="sxs-lookup"><span data-stu-id="caf4e-117">Subpicture</span></span>  |
| <span data-ttu-id="caf4e-118">5</span><span class="sxs-lookup"><span data-stu-id="caf4e-118">5</span></span>     | <span data-ttu-id="caf4e-119">звук;</span><span class="sxs-lookup"><span data-stu-id="caf4e-119">Audio</span></span>       |
| <span data-ttu-id="caf4e-120">6</span><span class="sxs-lookup"><span data-stu-id="caf4e-120">6</span></span>     | <span data-ttu-id="caf4e-121">Angle</span><span class="sxs-lookup"><span data-stu-id="caf4e-121">Angle</span></span>       |
| <span data-ttu-id="caf4e-122">7</span><span class="sxs-lookup"><span data-stu-id="caf4e-122">7</span></span>     | <span data-ttu-id="caf4e-123">Глава</span><span class="sxs-lookup"><span data-stu-id="caf4e-123">Chapter</span></span>     |



 

</dd> <dt>

<span data-ttu-id="caf4e-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*бенаблед*</span><span class="sxs-lookup"><span data-stu-id="caf4e-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="caf4e-125">Указывает, включена или отключена операция в качестве логического значения.</span><span class="sxs-lookup"><span data-stu-id="caf4e-125">Specifies whether the operation is enabled or disabled as a Boolean.</span></span>

</dd> </dl>

 

 



