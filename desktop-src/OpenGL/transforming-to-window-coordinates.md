---
title: Преобразование в координаты окна
description: Перед тем, как координаты обрезки преобразуются в координаты окна, они делятся на значение w, чтобы получить нормализованные координаты устройства.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Конвейер обработки OpenGL, преобразование в координаты окна
- Преобразование в координаты окна OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779460"
---
# <a name="transforming-to-window-coordinates"></a><span data-ttu-id="d69e6-105">Преобразование в координаты окна</span><span class="sxs-lookup"><span data-stu-id="d69e6-105">Transforming to Window Coordinates</span></span>

<span data-ttu-id="d69e6-106">Перед тем, как координаты обрезки преобразуются в координаты окна, они делятся на значение *w* , чтобы получить нормализованные координаты устройства.</span><span class="sxs-lookup"><span data-stu-id="d69e6-106">Before clip coordinates are converted to window coordinates, they are divided by the value of *w* to yield normalized device coordinates.</span></span> <span data-ttu-id="d69e6-107">Преобразование «окно просмотра», применяемое к этим нормализованным координатам, создает координаты окна.</span><span class="sxs-lookup"><span data-stu-id="d69e6-107">The viewport transformation applied to these normalized coordinates produces window coordinates.</span></span> <span data-ttu-id="d69e6-108">Вы управляете окном просмотра, которое определяет область экрана, в которой отображается изображение, с помощью [**глдепсранже**](gldepthrange.md) и [**глвиевпорт**](glviewport.md).</span><span class="sxs-lookup"><span data-stu-id="d69e6-108">You control the viewport, which determines the area of the on-screen window that displays an image, with [**glDepthRange**](gldepthrange.md) and [**glViewport**](glviewport.md).</span></span>

 

 




