---
description: Свойство BackColor задает или получает цвет полос, отображаемых вокруг краев прямоугольника видео, если пропорции изображения в машинном коде не совпадают с областью отображения объекта.
ms.assetid: 51576836-c648-4268-8475-0312dbd60963
title: Свойство BackColor (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37adb625080ca284c168c7286982e980f8919f3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655607"
---
# <a name="backcolor-property-directshow"></a><span data-ttu-id="37953-103">Свойство BackColor (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="37953-103">BackColor Property (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="37953-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="37953-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="37953-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="37953-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="37953-106">`BackColor`Свойство задает или получает цвет полос, отображаемых вокруг краев прямоугольника видео, если пропорции изображения в машинном коде не совпадают с областью отображения объекта.</span><span class="sxs-lookup"><span data-stu-id="37953-106">The `BackColor` property sets or retrieves the color of the bars that appear around the edges of the video rectangle when the aspect ratio of the native video is not the same as that of the object's display area.</span></span>

``` syntax
[ iBackColor = ] MSWebDVD.BackColor
```

## <a name="return-value"></a><span data-ttu-id="37953-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37953-107">Return Value</span></span>

<span data-ttu-id="37953-108">Возвращает целочисленное значение, представляющее RGB значения цвета фона.</span><span class="sxs-lookup"><span data-stu-id="37953-108">Returns an integer value representing the RGB values of the back color.</span></span>

## <a name="remarks"></a><span data-ttu-id="37953-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37953-109">Remarks</span></span>

<span data-ttu-id="37953-110">Это свойство доступно для чтения и записи со значением по умолчанию "Выкл-черный" (0x100010).</span><span class="sxs-lookup"><span data-stu-id="37953-110">This property is read/write with a default value of off-black (0x100010).</span></span>

 

 



