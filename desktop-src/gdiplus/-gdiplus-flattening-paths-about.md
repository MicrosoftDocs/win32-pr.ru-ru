---
description: Объект GraphicsPath сохраняет последовательность линий и B&\# 233; кривые Безье.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Сведение путей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988183"
---
# <a name="flattening-paths"></a><span data-ttu-id="e3d4c-103">Сведение путей</span><span class="sxs-lookup"><span data-stu-id="e3d4c-103">Flattening Paths</span></span>

<span data-ttu-id="e3d4c-104">Объект [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) хранит последовательность линий и сплайнов Безье.</span><span class="sxs-lookup"><span data-stu-id="e3d4c-104">A [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object stores a sequence of lines and Bézier splines.</span></span> <span data-ttu-id="e3d4c-105">К контуру можно добавить несколько типов кривых (эллипсы, дуги, фундаментальные сплайны), но каждая кривая преобразуется в кривую Безье, прежде чем она будет сохранена в пути.</span><span class="sxs-lookup"><span data-stu-id="e3d4c-105">You can add several types of curves (ellipses, arcs, cardinal splines) to a path, but each curve is converted to a Bézier spline before it is stored in the path.</span></span> <span data-ttu-id="e3d4c-106">Сведение контура состоит из преобразования каждого сплайна Безье в контуре в последовательность прямых линий.</span><span class="sxs-lookup"><span data-stu-id="e3d4c-106">Flattening a path consists of converting each Bézier spline in the path to a sequence of straight lines.</span></span>

<span data-ttu-id="e3d4c-107">Чтобы выполнить сведение пути, вызовите метод [**GraphicsPath:: спрямления**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) объекта [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="e3d4c-107">To flatten a path, call the [**GraphicsPath::Flatten**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="e3d4c-108">Метод **GraphicsPath:: спрямления** получает аргумент спрямления, указывающий максимальное расстояние между плоским путем и исходным путем.</span><span class="sxs-lookup"><span data-stu-id="e3d4c-108">The **GraphicsPath::Flatten** method receives a flatness argument that specifies the maximum distance between the flattened path and the original path.</span></span> <span data-ttu-id="e3d4c-109">На следующем рисунке показан путь до и после спрямления.</span><span class="sxs-lookup"><span data-stu-id="e3d4c-109">The following illustration shows a path before and after flattening.</span></span>

![Иллюстрация, показывающая последовательность Соединенных сплайнов Безье синим цветом и соответствующие линии в красном](images/aboutgdip02-art32a.png)

 

 



