---
description: API Direct3D определяет несколько элементов API, которые помогают создавать систему эффектов и управлять ею.
ms.assetid: d3b0b7a2-0820-4bb1-8b9e-c6b55a039963
title: Справочник по действиям (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c903959096e1192555fd813a256d03fb1969fa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990537"
---
# <a name="effect-reference-direct3d-10-graphics"></a><span data-ttu-id="cb473-103">Справочник по действиям (графика Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="cb473-103">Effect Reference (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="cb473-104">API Direct3D определяет несколько элементов API, которые помогают создавать систему эффектов и управлять ею.</span><span class="sxs-lookup"><span data-stu-id="cb473-104">The Direct3D API defines several API elements to help you create and manage the effect system.</span></span>

-   [<span data-ttu-id="cb473-105">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="cb473-105">Interfaces</span></span>](d3d10-graphics-reference-effect-interfaces.md)
-   [<span data-ttu-id="cb473-106">Функции</span><span class="sxs-lookup"><span data-stu-id="cb473-106">Functions</span></span>](d3d10-graphics-reference-effect-functions.md)
-   [<span data-ttu-id="cb473-107">Структуры</span><span class="sxs-lookup"><span data-stu-id="cb473-107">Structures</span></span>](d3d10-graphics-reference-effect-structures.md)
-   [<span data-ttu-id="cb473-108">Константы</span><span class="sxs-lookup"><span data-stu-id="cb473-108">Constants</span></span>](d3d10-graphics-reference-effect-constants.md)

<span data-ttu-id="cb473-109">Система влияния инкапсулирует назначения состояния в результате.</span><span class="sxs-lookup"><span data-stu-id="cb473-109">The effect system encapsulates state assignments in an effect.</span></span> <span data-ttu-id="cb473-110">Каждый результат — это коллекция состояния конвейера, которую можно разделить на назначения состояний с помощью блоков состояний, ресурсов и шейдеров.</span><span class="sxs-lookup"><span data-stu-id="cb473-110">Each effect is a collection of pipeline state which can be broken down into state assignments using state blocks, resources, and shaders.</span></span> <span data-ttu-id="cb473-111">В зависимости от размера результата можно реализовать его в текстовой строке ASCII или файле эффектов (. FX).</span><span class="sxs-lookup"><span data-stu-id="cb473-111">Depending on the size of an effect, you can choose to implement one in an ASCII text string or an effect file (.fx).</span></span> <span data-ttu-id="cb473-112">Чтобы упорядочить информацию в результате, см. [Формат эффектов](d3d10-effect-format.md).</span><span class="sxs-lookup"><span data-stu-id="cb473-112">To organize information in an effect, see the [effect format](d3d10-effect-format.md).</span></span>

<span data-ttu-id="cb473-113">Получив воздействие, используйте API эффектов, чтобы задать состояние на устройстве во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="cb473-113">Having designed an effect, use the effect API to set state in the device during rendering.</span></span> <span data-ttu-id="cb473-114">Кроме того, система эффектов поддерживает ряд API-интерфейсов отражения для получения и установки данных о последствиях.</span><span class="sxs-lookup"><span data-stu-id="cb473-114">As well, the effect system supports a series of reflection API's for getting and setting effect data.</span></span> <span data-ttu-id="cb473-115">Дополнительные сведения см. в разделе [воздействие системных интерфейсов (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="cb473-115">For more information, see [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb473-116">См. также</span><span class="sxs-lookup"><span data-stu-id="cb473-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb473-117">Справочник по Direct3D</span><span class="sxs-lookup"><span data-stu-id="cb473-117">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



