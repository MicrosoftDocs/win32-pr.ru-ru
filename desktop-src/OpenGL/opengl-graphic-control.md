---
title: Графический элемент управления OpenGL
description: Графический элемент управления OpenGL
ms.assetid: 327f2920-1bc9-4de7-aa12-3e9f74a94759
keywords:
- OpenGL, графический элемент управления
- графический элемент управления OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6bb138a2d8c597fae2d92a1d1394c8ff05b03cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776136"
---
# <a name="opengl-graphic-control"></a><span data-ttu-id="70738-105">Графический элемент управления OpenGL</span><span class="sxs-lookup"><span data-stu-id="70738-105">OpenGL Graphic Control</span></span>

<span data-ttu-id="70738-106">OpenGL обеспечивает довольно прямое управление фундаментальными операциями двух-и трехмерной графики.</span><span class="sxs-lookup"><span data-stu-id="70738-106">OpenGL provides you with fairly direct control over the fundamental operations of two- and three-dimensional graphics.</span></span> <span data-ttu-id="70738-107">Это включает в себя спецификацию таких параметров, как матрицы преобразования, коэффициенты освещения, методы сглаживания и операторы обновления пикселей.</span><span class="sxs-lookup"><span data-stu-id="70738-107">This includes specification of such parameters as transformation matrices, lighting equation coefficients, antialiasing methods, and pixel-update operators.</span></span> <span data-ttu-id="70738-108">Однако он не предоставляет средств для описания или моделирования сложных геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="70738-108">However, it doesn't provide you with a means for describing or modeling complex geometric objects.</span></span> <span data-ttu-id="70738-109">Таким образом, команды OpenGL, которые вы выдаете, указывают, как должен быть создан определенный результат (какая процедура должна следовать), а не то, как именно должен выглядеть результат.</span><span class="sxs-lookup"><span data-stu-id="70738-109">Thus, the OpenGL commands you issue specify how a certain result should be produced (what procedure should be followed) rather than what exactly that result should look like.</span></span> <span data-ttu-id="70738-110">Это значит, что OpenGL является фундаментальной процедурой, а не описательным.</span><span class="sxs-lookup"><span data-stu-id="70738-110">That is, OpenGL is fundamentally procedural rather than descriptive.</span></span> <span data-ttu-id="70738-111">Чтобы полностью понять, как использовать OpenGL, полезно знать порядок, в котором он выполняет операции.</span><span class="sxs-lookup"><span data-stu-id="70738-111">To fully understand how to use OpenGL, it helps to know the order in which it carries out its operations.</span></span>

 

 




