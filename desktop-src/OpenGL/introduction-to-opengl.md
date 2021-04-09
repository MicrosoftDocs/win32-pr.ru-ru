---
title: Введение в OpenGL
description: Введение в OpenGL
ms.assetid: 8fe214a9-f071-470b-ac72-182a7bd54fbd
keywords:
- OpenGL, введение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cece636e51348288e587116bf13f95696b93ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986343"
---
# <a name="introduction-to-opengl"></a><span data-ttu-id="2f09e-104">Введение в OpenGL</span><span class="sxs-lookup"><span data-stu-id="2f09e-104">Introduction to OpenGL</span></span>

<span data-ttu-id="2f09e-105">В качестве программного интерфейса для графического оборудования основной целью OpenGL является визуализация двух и трехмерных объектов в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2f09e-105">As a software interface for graphics hardware, the main purpose of OpenGL is to render two- and three-dimensional objects into a framebuffer.</span></span> <span data-ttu-id="2f09e-106">Эти объекты описаны в виде последовательностей вершин (определяющих геометрические объекты) или пикселов (определяющих изображения).</span><span class="sxs-lookup"><span data-stu-id="2f09e-106">These objects are described as sequences of vertices (that define geometric objects) or pixels (that define images).</span></span> <span data-ttu-id="2f09e-107">OpenGL выполняет несколько процессов с этими данными, чтобы преобразовать их в пиксели, чтобы сформировать окончательный требуемый образ в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2f09e-107">OpenGL performs several processes on this data to convert it to pixels to form the final desired image in the framebuffer.</span></span>

<span data-ttu-id="2f09e-108">В следующих разделах представлено глобальное представление о принципах работы OpenGL:</span><span class="sxs-lookup"><span data-stu-id="2f09e-108">The following topics present a global view of how OpenGL works:</span></span>

-   <span data-ttu-id="2f09e-109">[Примитивы и команды](primitives-and-commands.md) обсуждают точки, сегменты линии и многоугольники как базовые единицы рисования. и обработка команд.</span><span class="sxs-lookup"><span data-stu-id="2f09e-109">[Primitives and Commands](primitives-and-commands.md) discusses points, line segments, and polygons as the basic units of drawing; and the processing of commands.</span></span>
-   <span data-ttu-id="2f09e-110">[Графический элемент управления OpenGL](opengl-graphic-control.md) описывает графические операции с элементами управления OpenGL, которыми он не управляет.</span><span class="sxs-lookup"><span data-stu-id="2f09e-110">[OpenGL Graphic Control](opengl-graphic-control.md) describes which graphic operations OpenGL controls and which it does not control.</span></span>
-   <span data-ttu-id="2f09e-111">[Модель выполнения](execution-model.md) обсуждает модель "клиент-сервер" для интерпретации команд OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2f09e-111">[Execution Model](execution-model.md) discusses the client/server model for interpreting OpenGL commands.</span></span>
-   <span data-ttu-id="2f09e-112">[Базовая операция OpenGL](basic-opengl-operation.md) предоставляет высокоуровневое описание того, как OpenGL обрабатывает данные для получения соответствующего изображения в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2f09e-112">[Basic OpenGL Operation](basic-opengl-operation.md) gives a high-level description of how OpenGL processes data to produce a corresponding image in the framebuffer.</span></span>
-   <span data-ttu-id="2f09e-113">[Имена функций OpenGL](opengl-function-names.md) описание соглашений об именовании, используемых в OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2f09e-113">[OpenGL Function Names](opengl-function-names.md) describes the naming conventions used in OpenGL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f09e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2f09e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f09e-115">Конвейер обработки OpenGL</span><span class="sxs-lookup"><span data-stu-id="2f09e-115">OpenGL Processing Pipeline</span></span>](opengl-processing-pipeline.md)
</dt> <dt>

[<span data-ttu-id="2f09e-116">Использование оценивающих</span><span class="sxs-lookup"><span data-stu-id="2f09e-116">Using Evaluators</span></span>](using-evaluators.md)
</dt> <dt>

[<span data-ttu-id="2f09e-117">Выполнив выбор и обратную связь</span><span class="sxs-lookup"><span data-stu-id="2f09e-117">Performing Selection and Feedback</span></span>](performing-selection-and-feedback.md)
</dt> <dt>

[<span data-ttu-id="2f09e-118">Использование списков вывода</span><span class="sxs-lookup"><span data-stu-id="2f09e-118">Using Display Lists</span></span>](using-display-lists.md)
</dt> <dt>

[<span data-ttu-id="2f09e-119">Управление режимами и выполнением</span><span class="sxs-lookup"><span data-stu-id="2f09e-119">Managing Modes and Execution</span></span>](managing-modes-and-execution.md)
</dt> <dt>

[<span data-ttu-id="2f09e-120">Получение сведений о состоянии</span><span class="sxs-lookup"><span data-stu-id="2f09e-120">Obtaining State Information</span></span>](obtaining-state-information.md)
</dt> <dt>

[<span data-ttu-id="2f09e-121">Библиотека служебной программы OpenGL</span><span class="sxs-lookup"><span data-stu-id="2f09e-121">OpenGL Utility Library</span></span>](opengl-utility-library.md)
</dt> </dl>

 

 




