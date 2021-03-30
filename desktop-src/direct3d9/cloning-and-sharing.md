---
description: Клонирование и совместное использование (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Клонирование и совместное использование (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896398"
---
# <a name="cloning-and-sharing-direct3d-9"></a><span data-ttu-id="e333c-103">Клонирование и совместное использование (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e333c-103">Cloning and Sharing (Direct3D 9)</span></span>

## <a name="cloning-parameters"></a><span data-ttu-id="e333c-104">Клонирование параметров</span><span class="sxs-lookup"><span data-stu-id="e333c-104">Cloning Parameters</span></span>

<span data-ttu-id="e333c-105">Клонирование имеет следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="e333c-105">Cloning has the following restrictions.</span></span>

-   <span data-ttu-id="e333c-106">Клоны наследуют пул исходного воздействия.</span><span class="sxs-lookup"><span data-stu-id="e333c-106">Clones inherit the original effect's pool.</span></span> <span data-ttu-id="e333c-107">См. раздел Параметры совместного использования.</span><span class="sxs-lookup"><span data-stu-id="e333c-107">See the Sharing Parameters section.</span></span>
-   <span data-ttu-id="e333c-108">Клоны наследуют методы исходного воздействия, передают, параметры и заметки (включая все заметки, добавленные с помощью [**ID3DXEffect**](id3dxeffect.md)).</span><span class="sxs-lookup"><span data-stu-id="e333c-108">Clones inherit the original effect's techniques, passes, parameters, and annotations (including all annotations added with [**ID3DXEffect**](id3dxeffect.md)).</span></span>
-   <span data-ttu-id="e333c-109">Клоны наследуют заметки, динамически добавляемые к исходному результату.</span><span class="sxs-lookup"><span data-stu-id="e333c-109">Clones inherit the original effect's dynamically added annotations.</span></span>
-   <span data-ttu-id="e333c-110">Клонирование на новое устройство завершится ошибкой, если пул исходных эффектов не **равен null** и исходный результат содержал общий зависимый от устройства параметр (например, текстуру или шейдер).</span><span class="sxs-lookup"><span data-stu-id="e333c-110">Cloning onto a new device will fail if the original effect's pool was not **NULL** and the original effect contained a shared device-dependent parameter (such as a texture or shader).</span></span>

## <a name="sharing-parameters"></a><span data-ttu-id="e333c-111">Совместное использование параметров</span><span class="sxs-lookup"><span data-stu-id="e333c-111">Sharing Parameters</span></span>

<span data-ttu-id="e333c-112">Пул — это буфер, который предоставляет общий доступ к параметрам различных эффектов.</span><span class="sxs-lookup"><span data-stu-id="e333c-112">A pool is a buffer that shares effect parameters between different effects.</span></span> <span data-ttu-id="e333c-113">Чтобы добавить параметры в пул, укажите общее использование при создании этого результата.</span><span class="sxs-lookup"><span data-stu-id="e333c-113">To add parameters to a pool, specify a shared usage when the effect is created.</span></span>

<span data-ttu-id="e333c-114">У пула есть следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="e333c-114">A pool has the following restrictions.</span></span>

-   <span data-ttu-id="e333c-115">Параметр добавляется в пул при первом добавлении в пул результата, содержащего этот параметр (Shared).</span><span class="sxs-lookup"><span data-stu-id="e333c-115">A parameter is added to the pool the first time an effect containing that (shared) parameter is added to the pool.</span></span>
-   <span data-ttu-id="e333c-116">Пул получает начальные значения из первого общего параметра; Общие параметры последующего получения значений из пула.</span><span class="sxs-lookup"><span data-stu-id="e333c-116">A pool gets initial values from the first shared parameter; parameters shared subsequently get their values from the pool.</span></span>
-   <span data-ttu-id="e333c-117">Параметр удаляется из пула, когда освобождаются все ссылки на общий параметр.</span><span class="sxs-lookup"><span data-stu-id="e333c-117">A parameter is deleted from the pool when all effect references to the shared parameter are released.</span></span>
-   <span data-ttu-id="e333c-118">Все эффекты в пуле, которые содержат одинаковый (общий) зависимый от устройства параметр, должны иметь одно и то же устройство.</span><span class="sxs-lookup"><span data-stu-id="e333c-118">All effects in the pool that contain the same (shared) device-dependent parameter must have the same device.</span></span>

<span data-ttu-id="e333c-119">**Null** можно использовать для указания отсутствия пула, в этом случае параметры не являются общими.</span><span class="sxs-lookup"><span data-stu-id="e333c-119">**NULL** can be used to specify no pool, in which case no parameters are shared.</span></span> <span data-ttu-id="e333c-120">Это почти эквивалентно указанию уникального пула только для этого результата.</span><span class="sxs-lookup"><span data-stu-id="e333c-120">This is almost equivalent to specifying a unique pool just for this effect.</span></span> <span data-ttu-id="e333c-121">Единственное отличие состоит в том, что при клонировании результата клон не будет совместно использовать его общие параметры с исходным.</span><span class="sxs-lookup"><span data-stu-id="e333c-121">The single difference is that when the effect is cloned, the clone will not share its shared parameters with the original.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e333c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e333c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e333c-123">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="e333c-123">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



