---
title: Иажентнотифисинк Драгстарт
description: Иажентнотифисинк Драгстарт
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120828"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="03baa-103">Иажентнотифисинк::D Рагстарт</span><span class="sxs-lookup"><span data-stu-id="03baa-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="03baa-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="03baa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="03baa-105">Уведомляет клиентское приложение, когда пользователь начинает перетаскивать символ.</span><span class="sxs-lookup"><span data-stu-id="03baa-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="03baa-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="03baa-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="03baa-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="03baa-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="03baa-108">Идентификатор перетаскиваемого символа.</span><span class="sxs-lookup"><span data-stu-id="03baa-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="03baa-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*фвкэйс*</span><span class="sxs-lookup"><span data-stu-id="03baa-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="03baa-110">Параметр, указывающий кнопку мыши и состояние клавиши-модификатора.</span><span class="sxs-lookup"><span data-stu-id="03baa-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="03baa-111">Параметр может возвращать любое сочетание следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="03baa-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="03baa-112">Значение</span><span class="sxs-lookup"><span data-stu-id="03baa-112">Value</span></span>  | <span data-ttu-id="03baa-113">Описание</span><span class="sxs-lookup"><span data-stu-id="03baa-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="03baa-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="03baa-114">0x0001</span></span> | <span data-ttu-id="03baa-115">Левая кнопка</span><span class="sxs-lookup"><span data-stu-id="03baa-115">Left Button</span></span>      |
| <span data-ttu-id="03baa-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="03baa-116">0x0010</span></span> | <span data-ttu-id="03baa-117">Средняя кнопка</span><span class="sxs-lookup"><span data-stu-id="03baa-117">Middle Button</span></span>    |
| <span data-ttu-id="03baa-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="03baa-118">0x0002</span></span> | <span data-ttu-id="03baa-119">Правая кнопка</span><span class="sxs-lookup"><span data-stu-id="03baa-119">Right Button</span></span>     |
| <span data-ttu-id="03baa-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="03baa-120">0x0004</span></span> | <span data-ttu-id="03baa-121">Shift + стрелка вниз</span><span class="sxs-lookup"><span data-stu-id="03baa-121">Shift Key Down</span></span>   |
| <span data-ttu-id="03baa-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="03baa-122">0x0008</span></span> | <span data-ttu-id="03baa-123">Клавиша управления</span><span class="sxs-lookup"><span data-stu-id="03baa-123">Control Key Down</span></span> |
| <span data-ttu-id="03baa-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="03baa-124">0x0020</span></span> | <span data-ttu-id="03baa-125">Клавиша Alt</span><span class="sxs-lookup"><span data-stu-id="03baa-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="03baa-126"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="03baa-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="03baa-127">Координата по оси x указателя мыши в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="03baa-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="03baa-128"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="03baa-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="03baa-129">Координата по оси y указателя мыши в пикселях относительно начала координат экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="03baa-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




