---
description: Свойство Куррентволуме извлекает номер тома для текущего корневого каталога.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Куррентволуме, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672961"
---
# <a name="currentvolume-property"></a><span data-ttu-id="8ce28-103">Куррентволуме, свойство</span><span class="sxs-lookup"><span data-stu-id="8ce28-103">CurrentVolume Property</span></span>

> [!Note]  
> <span data-ttu-id="8ce28-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8ce28-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8ce28-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="8ce28-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8ce28-106">`CurrentVolume`Свойство получает номер тома для текущего корневого каталога.</span><span class="sxs-lookup"><span data-stu-id="8ce28-106">The `CurrentVolume` property retrieves the volume number for the current root directory.</span></span>

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a><span data-ttu-id="8ce28-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ce28-107">Return Value</span></span>

<span data-ttu-id="8ce28-108">Возвращает целочисленное значение, представляющее текущий том DVD.</span><span class="sxs-lookup"><span data-stu-id="8ce28-108">Returns an integer value representing the current DVD volume.</span></span> <span data-ttu-id="8ce28-109">Если диск входит в состав набора из нескольких томов, то целочисленное значение должно быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="8ce28-109">If a disc is part of a multi-volume set, then the integer value should be greater than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ce28-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ce28-110">Remarks</span></span>

<span data-ttu-id="8ce28-111">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ce28-111">This property is read-only with no default value.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ce28-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ce28-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce28-113">**волумесаваилабле**</span><span class="sxs-lookup"><span data-stu-id="8ce28-113">**VolumesAvailable**</span></span>](volumesavailable-property.md)
</dt> </dl>

 

 



