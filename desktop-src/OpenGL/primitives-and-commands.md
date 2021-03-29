---
title: Примитивы и команды
description: Примитивы и команды
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, примитивы
- OpenGL, команды
- примитивы OpenGL
- команды OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774996"
---
# <a name="primitives-and-commands"></a><span data-ttu-id="640bb-107">Примитивы и команды</span><span class="sxs-lookup"><span data-stu-id="640bb-107">Primitives and Commands</span></span>

<span data-ttu-id="640bb-108">OpenGL рисует точки *примитивов* , сегменты линии или полигонссубжект в нескольких выбираемых режимах.</span><span class="sxs-lookup"><span data-stu-id="640bb-108">OpenGL draws *primitives* points, line segments, or polygonssubject to several selectable modes.</span></span> <span data-ttu-id="640bb-109">Вы можете управлять режимами независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="640bb-109">You can control modes independently of one another.</span></span> <span data-ttu-id="640bb-110">Это значит, что установка одного режима не влияет на то, установлены ли другие режимы (хотя многие режимы могут взаимодействовать, чтобы определить, что в итоге заканчивается в буфера кадров).</span><span class="sxs-lookup"><span data-stu-id="640bb-110">That is, setting one mode doesn't affect whether other modes are set (although many modes may interact to determine what eventually ends up in the framebuffer).</span></span> <span data-ttu-id="640bb-111">Для указания примитивов, режимов установки и выполнения других операций OpenGL команды выполняются в форме вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="640bb-111">To specify primitives, set modes, and perform other OpenGL operations, you issue commands in the form of function calls.</span></span>

<span data-ttu-id="640bb-112">Примитивы определяются группой из одной или нескольких *вершин*.</span><span class="sxs-lookup"><span data-stu-id="640bb-112">Primitives are defined by a group of one or more *vertices*.</span></span> <span data-ttu-id="640bb-113">Вершина определяет точку, конечную точку линии или угол многоугольника, на котором встречаются два края.</span><span class="sxs-lookup"><span data-stu-id="640bb-113">A vertex defines a point, an endpoint of a line, or a corner of a polygon where two edges meet.</span></span> <span data-ttu-id="640bb-114">Данные (состоящие из координат вершин, цветов, нормалей, координат текстуры и пограничных флагов) связаны с вершиной, и каждая вершина и связанные с ней данные обрабатываются независимо друг от друга, по порядку и тем же способом.</span><span class="sxs-lookup"><span data-stu-id="640bb-114">Data (consisting of vertex coordinates, colors, normals, texture coordinates, and edge flags) is associated with a vertex, and each vertex and its associated data are processed independently, in order, and in the same way.</span></span> <span data-ttu-id="640bb-115">Единственным исключением из этого правила являются случаи, в которых группа вершин должна быть обрезана, чтобы конкретный примитив поместились в указанную область.</span><span class="sxs-lookup"><span data-stu-id="640bb-115">The only exceptions to this rule are cases in which the group of vertices must be clipped so that a particular primitive fits within a specified region.</span></span> <span data-ttu-id="640bb-116">В этом случае можно изменить данные вершин и создать новые вершины.</span><span class="sxs-lookup"><span data-stu-id="640bb-116">In this case, vertex data may be modified and new vertices created.</span></span> <span data-ttu-id="640bb-117">Тип обрезки зависит от того, какой примитив представляет группа вершин.</span><span class="sxs-lookup"><span data-stu-id="640bb-117">The type of clipping depends on which primitive the group of vertices represents.</span></span>

<span data-ttu-id="640bb-118">Команды всегда обрабатываются в порядке их получения, хотя до вступления в силу команды может возникнуть неопределенная задержка.</span><span class="sxs-lookup"><span data-stu-id="640bb-118">Commands are always processed in the order in which they are received, although there may be an indeterminate delay before a command takes effect.</span></span> <span data-ttu-id="640bb-119">Это означает, что каждый примитив выводится полностью до вступления в силу любой последующей команды.</span><span class="sxs-lookup"><span data-stu-id="640bb-119">This means that each primitive is drawn completely before any subsequent command takes effect.</span></span> <span data-ttu-id="640bb-120">Это также означает, что команды запроса состояния возвращают данные, которые соответствуют полному выполнению всех ранее выданных команд OpenGL.</span><span class="sxs-lookup"><span data-stu-id="640bb-120">It also means that state-querying commands return data that is consistent with complete execution of all previously issued OpenGL commands.</span></span>

 

 




