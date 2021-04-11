---
description: 'Положение, скорость и ориентация звуковых источников и прослушивателей в трехмерном пространстве представлены декартыми координатами, которые являются значениями на трех осях: ось x, ось y и ось z.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Координаты трехмерного пространства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265272"
---
# <a name="coordinates-of-3d-space"></a><span data-ttu-id="33ec7-103">Координаты трехмерного пространства</span><span class="sxs-lookup"><span data-stu-id="33ec7-103">Coordinates of 3D Space</span></span>

<span data-ttu-id="33ec7-104">Положение, скорость и ориентация звуковых источников и прослушивателей в трехмерном пространстве представлены декартыми координатами, которые являются значениями на трех осях: ось x, ось y и ось z.</span><span class="sxs-lookup"><span data-stu-id="33ec7-104">The position, velocity, and orientation of sound sources and listeners in 3D space are represented by Cartesian coordinates, which are values on three axes: the x-axis, the y-axis, and the z-axis.</span></span>

<span data-ttu-id="33ec7-105">Оси задаются относительно точек зрения, установленных приложением.</span><span class="sxs-lookup"><span data-stu-id="33ec7-105">The axes are relative to a viewpoint established by the application.</span></span> <span data-ttu-id="33ec7-106">Значения на оси x увеличиваются слева направо, на оси y — сверху вниз, а на оси z — от ближайшего к Дальнему.</span><span class="sxs-lookup"><span data-stu-id="33ec7-106">Values on the x-axis increase from left to right, on the y-axis from down to up, and on the z-axis from near to far.</span></span>

<span data-ttu-id="33ec7-107">Структура **\_ вектора X3DAUDIO** содержит значения, описывающие положение, скорость или ориентацию по трем осям.</span><span class="sxs-lookup"><span data-stu-id="33ec7-107">The **X3DAUDIO\_VECTOR** structure contains values describing position, velocity, or orientation on the three axes.</span></span>

<span data-ttu-id="33ec7-108">В соответствии с соглашениями, векторы выражаются как три значения, заключенные в круглые скобки и разделенные запятыми, в порядке (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="33ec7-108">Conventionally, vectors are expressed as three values enclosed in parentheses and separated by commas, in the order (x, y, z).</span></span>

<span data-ttu-id="33ec7-109">Для позиций значения находятся в определяемых пользователем универсальных единицах.</span><span class="sxs-lookup"><span data-stu-id="33ec7-109">For position, the values are in user-defined world units.</span></span>

<span data-ttu-id="33ec7-110">Для скорости вектор описывает скорость движения по каждой оси в мировых единицах в секунду.</span><span class="sxs-lookup"><span data-stu-id="33ec7-110">For velocity, the vector describes the rate of movement along each axis in world units per second.</span></span>

<span data-ttu-id="33ec7-111">Для ориентации значения находятся в произвольных единицах и зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="33ec7-111">For orientation, the values are in arbitrary units, and they are relative to one another.</span></span> <span data-ttu-id="33ec7-112">Например, если базовое представление трехмерного мира приближается к горизонту, а ориентация прослушивателя — (-1, 0, 1), то прослушиватель становится северо-западом.</span><span class="sxs-lookup"><span data-stu-id="33ec7-112">For example, if the base view of the 3D world is facing north toward the horizon, and the orientation of the listener is (-1, 0, 1), then the listener is facing northwest.</span></span> <span data-ttu-id="33ec7-113">Поскольку значения в векторе находятся не в абсолютных единицах, вектор может быть выражен как (-5, 0, 5) или (-0,25, 0, 0,25).</span><span class="sxs-lookup"><span data-stu-id="33ec7-113">Because the values within a vector are not in absolute units, the vector equally could be expressed as (-5, 0, 5) or (-0.25, 0, 0.25).</span></span>

<span data-ttu-id="33ec7-114">Трехмерные векторы работают примерно так же, как Двумерные векторы, но с дополнительной осью в направлении вверх-вниз.</span><span class="sxs-lookup"><span data-stu-id="33ec7-114">3D vectors work much like 2D vectors, but with an additional axis in the up-down direction.</span></span> <span data-ttu-id="33ec7-115">Вы видите, как векторы работают в двухмерном пространстве, рисуя их на листе бумаги.</span><span class="sxs-lookup"><span data-stu-id="33ec7-115">You can see how vectors work in 2D space by drawing them on a sheet of graph paper.</span></span> <span data-ttu-id="33ec7-116">Разрешите, что значения повышаются в верхней части бумаги и слева направо.</span><span class="sxs-lookup"><span data-stu-id="33ec7-116">Let the values increase from the bottom to the top of the paper, and from left to right.</span></span> <span data-ttu-id="33ec7-117">Линия, нарисованная от (0, 0) до (1, 1), имеет одинаковую ориентацию или направление, как одно из (0, 0) до (5, 5).</span><span class="sxs-lookup"><span data-stu-id="33ec7-117">A line drawn from (0, 0) to (1, 1) has the same orientation, or direction, as one drawn from (0, 0) to (5, 5).</span></span> <span data-ttu-id="33ec7-118">Однако вторая строка указывает на большее расстояние или скорость.</span><span class="sxs-lookup"><span data-stu-id="33ec7-118">However, the second line indicates a greater distance, or velocity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33ec7-119">См. также</span><span class="sxs-lookup"><span data-stu-id="33ec7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33ec7-120">Общие концепции аудио</span><span class="sxs-lookup"><span data-stu-id="33ec7-120">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="33ec7-121">Обзор X3DAudio</span><span class="sxs-lookup"><span data-stu-id="33ec7-121">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> </dl>

 

 



