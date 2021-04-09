---
title: Иажентнотифисинк Драгкомплете
description: Иажентнотифисинк Драгкомплете
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53215591e3d2797c5b57e5586ccb13fc91f5902
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068492"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="9cc05-103">Иажентнотифисинк::D Рагкомплете</span><span class="sxs-lookup"><span data-stu-id="9cc05-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="9cc05-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9cc05-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="9cc05-105">Уведомляет клиентское приложение, когда пользователь прекращает перетаскивание символа.</span><span class="sxs-lookup"><span data-stu-id="9cc05-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="9cc05-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="9cc05-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="9cc05-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="9cc05-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="9cc05-108">Идентификатор перетаскиваемого символа.</span><span class="sxs-lookup"><span data-stu-id="9cc05-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="9cc05-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*фвкэйс*</span><span class="sxs-lookup"><span data-stu-id="9cc05-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="9cc05-110">Параметр, указывающий кнопку мыши и состояние клавиши-модификатора.</span><span class="sxs-lookup"><span data-stu-id="9cc05-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="9cc05-111">Параметр может возвращать любое сочетание следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="9cc05-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="9cc05-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="9cc05-112">0x0001</span></span> | <span data-ttu-id="9cc05-113">Левая кнопка</span><span class="sxs-lookup"><span data-stu-id="9cc05-113">Left Button</span></span>      |
| <span data-ttu-id="9cc05-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="9cc05-114">0x0010</span></span> | <span data-ttu-id="9cc05-115">Средняя кнопка</span><span class="sxs-lookup"><span data-stu-id="9cc05-115">Middle Button</span></span>    |
| <span data-ttu-id="9cc05-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="9cc05-116">0x0002</span></span> | <span data-ttu-id="9cc05-117">Правая кнопка</span><span class="sxs-lookup"><span data-stu-id="9cc05-117">Right Button</span></span>     |
| <span data-ttu-id="9cc05-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="9cc05-118">0x0004</span></span> | <span data-ttu-id="9cc05-119">Shift + стрелка вниз</span><span class="sxs-lookup"><span data-stu-id="9cc05-119">Shift Key Down</span></span>   |
| <span data-ttu-id="9cc05-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="9cc05-120">0x0008</span></span> | <span data-ttu-id="9cc05-121">Клавиша управления</span><span class="sxs-lookup"><span data-stu-id="9cc05-121">Control Key Down</span></span> |
| <span data-ttu-id="9cc05-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="9cc05-122">0x0020</span></span> | <span data-ttu-id="9cc05-123">Клавиша Alt</span><span class="sxs-lookup"><span data-stu-id="9cc05-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="9cc05-124"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="9cc05-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="9cc05-125">Координата по оси x указателя мыши в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="9cc05-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="9cc05-126"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="9cc05-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="9cc05-127">Координата по оси y указателя мыши в пикселях относительно начала координат экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="9cc05-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




