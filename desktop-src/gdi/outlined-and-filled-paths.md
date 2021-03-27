---
description: Приложение может нарисовать контур пути путем вызова функции Строкепас, он может заполнить внутреннюю часть пути путем вызова функции Филлпас, и она может как структурировать, так и заполнять путь путем вызова функции Строкеандфиллпас.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Контуры и заливки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991493"
---
# <a name="outlined-and-filled-paths"></a><span data-ttu-id="8581d-103">Контуры и заливки</span><span class="sxs-lookup"><span data-stu-id="8581d-103">Outlined and Filled Paths</span></span>

<span data-ttu-id="8581d-104">Приложение может нарисовать контур пути путем вызова функции [**строкепас**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , он может заполнить внутреннюю часть пути путем вызова функции [**филлпас**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) , и она может как структурировать, так и заполнять путь путем вызова функции [**строкеандфиллпас**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .</span><span class="sxs-lookup"><span data-stu-id="8581d-104">An application can draw the outline of a path by calling the [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) function, it can fill the interior of a path by calling the [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) function, and it can both outline and fill the path by calling the [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) function.</span></span>

<span data-ttu-id="8581d-105">Всякий раз, когда приложение заполняет путь, система использует текущий режим заполнения контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="8581d-105">Whenever an application fills a path, the system uses the DC's current fill mode.</span></span> <span data-ttu-id="8581d-106">Приложение может получить этот режим, вызвав функцию [**жетполифиллмоде**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) , и установить новый режим заполнения, вызвав функцию [**сетполифиллмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="8581d-106">An application can retrieve this mode by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function, and it can set a new fill mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="8581d-107">Описание двух режимов заливки см. в разделе [регионы](regions.md).</span><span class="sxs-lookup"><span data-stu-id="8581d-107">For a description of the two fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="8581d-108">На следующем рисунке показана перекрестная часть объекта, созданного приложением для автоматизированного проектирования (CAD), с использованием контуров, которые были выкрашены и заполнены.</span><span class="sxs-lookup"><span data-stu-id="8581d-108">The following illustration shows the cross-section of an object created by a computer-aided design (CAD) application using paths that were both outlined and filled.</span></span>

![Иллюстрация, показывающая перекрестное представление объекта с различными частями, определяемыми различными шаблонами заливки](images/cspth-01.png)

 

 



