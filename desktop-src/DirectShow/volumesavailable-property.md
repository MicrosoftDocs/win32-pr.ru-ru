---
description: Свойство Волумесаваилабле извлекает количество томов в наборе из нескольких томов.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Волумесаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683766"
---
# <a name="volumesavailable-property"></a><span data-ttu-id="a08a5-103">Волумесаваилабле, свойство</span><span class="sxs-lookup"><span data-stu-id="a08a5-103">VolumesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="a08a5-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a08a5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a08a5-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="a08a5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a08a5-106">`VolumesAvailable`Свойство получает количество томов в многотомном наборе.</span><span class="sxs-lookup"><span data-stu-id="a08a5-106">The `VolumesAvailable` property retrieves the number of volumes in a multivolume set.</span></span>

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a><span data-ttu-id="a08a5-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a08a5-107">Return Value</span></span>

<span data-ttu-id="a08a5-108">Возвращает количество томов в наборе в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="a08a5-108">Returns the number of volumes in the set as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="a08a5-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a08a5-109">Remarks</span></span>

<span data-ttu-id="a08a5-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a08a5-110">This property is read-only with no default value.</span></span> <span data-ttu-id="a08a5-111">Некоторые заголовки DVD могут быть выпущены в виде набора или ряда с несколькими дисками.</span><span class="sxs-lookup"><span data-stu-id="a08a5-111">Some DVD titles might be released as a multidisc set or series.</span></span> <span data-ttu-id="a08a5-112">Используйте этот метод, чтобы определить номер тома для текущего диска.</span><span class="sxs-lookup"><span data-stu-id="a08a5-112">Use this method to determine the volume number for the current disc.</span></span>

 

 



