---
description: Метод Жетвидеосизе извлекает собственные измерения видео.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Метод Жетвидеосизе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673103"
---
# <a name="getvideosize-method"></a><span data-ttu-id="ded1d-103">Метод Жетвидеосизе</span><span class="sxs-lookup"><span data-stu-id="ded1d-103">GetVideoSize Method</span></span>

> [!Note]  
> <span data-ttu-id="ded1d-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ded1d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ded1d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="ded1d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ded1d-106">`GetVideoSize`Метод получает собственные измерения видео.</span><span class="sxs-lookup"><span data-stu-id="ded1d-106">The `GetVideoSize` method retrieves the native video dimensions.</span></span>

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a><span data-ttu-id="ded1d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ded1d-107">Return Value</span></span>

<span data-ttu-id="ded1d-108">Возвращает объект [двдрект](dvdrect-object.md) , содержащий четыре свойства для чтения и записи: (сверху слева) x; (сверху слева) y, Width и Height.</span><span class="sxs-lookup"><span data-stu-id="ded1d-108">Returns a [DVDRect](dvdrect-object.md) object containing four read/write properties: (top left) x; (top left) y, Width, and Height.</span></span> <span data-ttu-id="ded1d-109">Свойства **x** и **y** имеют нулевое значение, а другие два свойства соответствуют ширине и высоте видеопрямоугольника, созданного на диске.</span><span class="sxs-lookup"><span data-stu-id="ded1d-109">The **x** and **y** properties are set to zero and the other two properties reflect the width and height of the video rectangle as authored on the disc.</span></span>

 

 



