---
title: Иажентнотифисинк Драгкомплете
description: Иажентнотифисинк Драгкомплете
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb93fbc7bae1ac43d534962659b850561bd50a6d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120809"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="fd3c2-103">Иажентнотифисинк::D Рагкомплете</span><span class="sxs-lookup"><span data-stu-id="fd3c2-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="fd3c2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd3c2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="fd3c2-105">Уведомляет клиентское приложение, когда пользователь прекращает перетаскивание символа.</span><span class="sxs-lookup"><span data-stu-id="fd3c2-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="fd3c2-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fd3c2-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="fd3c2-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="fd3c2-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="fd3c2-108">Идентификатор перетаскиваемого символа.</span><span class="sxs-lookup"><span data-stu-id="fd3c2-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="fd3c2-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*фвкэйс*</span><span class="sxs-lookup"><span data-stu-id="fd3c2-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="fd3c2-110">Параметр, указывающий кнопку мыши и состояние клавиши-модификатора.</span><span class="sxs-lookup"><span data-stu-id="fd3c2-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="fd3c2-111">Параметр может возвращать любое сочетание следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="fd3c2-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="fd3c2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="fd3c2-112">Value</span></span>  | <span data-ttu-id="fd3c2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="fd3c2-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="fd3c2-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="fd3c2-114">0x0001</span></span> | <span data-ttu-id="fd3c2-115">Левая кнопка</span><span class="sxs-lookup"><span data-stu-id="fd3c2-115">Left Button</span></span>      |
| <span data-ttu-id="fd3c2-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="fd3c2-116">0x0010</span></span> | <span data-ttu-id="fd3c2-117">Средняя кнопка</span><span class="sxs-lookup"><span data-stu-id="fd3c2-117">Middle Button</span></span>    |
| <span data-ttu-id="fd3c2-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="fd3c2-118">0x0002</span></span> | <span data-ttu-id="fd3c2-119">Правая кнопка</span><span class="sxs-lookup"><span data-stu-id="fd3c2-119">Right Button</span></span>     |
| <span data-ttu-id="fd3c2-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="fd3c2-120">0x0004</span></span> | <span data-ttu-id="fd3c2-121">Shift + стрелка вниз</span><span class="sxs-lookup"><span data-stu-id="fd3c2-121">Shift Key Down</span></span>   |
| <span data-ttu-id="fd3c2-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="fd3c2-122">0x0008</span></span> | <span data-ttu-id="fd3c2-123">Клавиша управления</span><span class="sxs-lookup"><span data-stu-id="fd3c2-123">Control Key Down</span></span> |
| <span data-ttu-id="fd3c2-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="fd3c2-124">0x0020</span></span> | <span data-ttu-id="fd3c2-125">Клавиша Alt</span><span class="sxs-lookup"><span data-stu-id="fd3c2-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="fd3c2-126"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="fd3c2-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="fd3c2-127">Координата по оси x указателя мыши в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="fd3c2-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="fd3c2-128"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="fd3c2-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="fd3c2-129">Координата по оси y указателя мыши в пикселях относительно начала координат экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="fd3c2-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




