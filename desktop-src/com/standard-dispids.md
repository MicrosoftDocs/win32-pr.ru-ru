---
title: Стандартные идентификаторы DISPID
description: Для спецификации элементов управления определено несколько стандартных идентификаторов DISPID.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700515"
---
# <a name="standard-dispids"></a><span data-ttu-id="daa41-103">Стандартные идентификаторы DISPID</span><span class="sxs-lookup"><span data-stu-id="daa41-103">Standard DISPIDS</span></span>

<span data-ttu-id="daa41-104">Для спецификации элементов управления определено несколько стандартных идентификаторов DISPID.</span><span class="sxs-lookup"><span data-stu-id="daa41-104">A number of standard dispids have been defined for the controls specification.</span></span>

## <a name="dispid_mousepointer"></a><span data-ttu-id="daa41-105">Идентификатор DISPID \_ MOUSEPOINTER</span><span class="sxs-lookup"><span data-stu-id="daa41-105">DISPID\_MOUSEPOINTER</span></span>

<span data-ttu-id="daa41-106">Свойство целочисленного типа.</span><span class="sxs-lookup"><span data-stu-id="daa41-106">Property of type integer.</span></span>

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

<span data-ttu-id="daa41-107">Свойство MousePointer определяет стандартные значки мыши.</span><span class="sxs-lookup"><span data-stu-id="daa41-107">The Mousepointer property identifies standard mouse icons.</span></span>



| <span data-ttu-id="daa41-108">Значение</span><span class="sxs-lookup"><span data-stu-id="daa41-108">Value</span></span>         | <span data-ttu-id="daa41-109">Описание</span><span class="sxs-lookup"><span data-stu-id="daa41-109">Description</span></span>                                                                |
|---------------|----------------------------------------------------------------------------|
| <span data-ttu-id="daa41-110">0</span><span class="sxs-lookup"><span data-stu-id="daa41-110">0</span></span><br/>  | <span data-ttu-id="daa41-111">Параметры Фигура, определяемая объектом.</span><span class="sxs-lookup"><span data-stu-id="daa41-111">(Default) Shape determined by the object.</span></span><br/>                       |
| <span data-ttu-id="daa41-112">1</span><span class="sxs-lookup"><span data-stu-id="daa41-112">1</span></span><br/>  | <span data-ttu-id="daa41-113">Стрелка</span><span class="sxs-lookup"><span data-stu-id="daa41-113">Arrow</span></span><br/>                                                           |
| <span data-ttu-id="daa41-114">2</span><span class="sxs-lookup"><span data-stu-id="daa41-114">2</span></span><br/>  | <span data-ttu-id="daa41-115">Крестик (перекрестный указатель)</span><span class="sxs-lookup"><span data-stu-id="daa41-115">Cross (cross-hair pointer)</span></span><br/>                                      |
| <span data-ttu-id="daa41-116">3</span><span class="sxs-lookup"><span data-stu-id="daa41-116">3</span></span><br/>  | <span data-ttu-id="daa41-117">I</span><span class="sxs-lookup"><span data-stu-id="daa41-117">I Beam</span></span><br/>                                                          |
| <span data-ttu-id="daa41-118">4</span><span class="sxs-lookup"><span data-stu-id="daa41-118">4</span></span><br/>  | <span data-ttu-id="daa41-119">Значок (маленький квадрат в квадрате)</span><span class="sxs-lookup"><span data-stu-id="daa41-119">Icon (small square within a square)</span></span><br/>                             |
| <span data-ttu-id="daa41-120">5</span><span class="sxs-lookup"><span data-stu-id="daa41-120">5</span></span><br/>  | <span data-ttu-id="daa41-121">Размер (четырехконечная стрелка, указывающая на север, Юг, Восток и Западная)</span><span class="sxs-lookup"><span data-stu-id="daa41-121">Size (four-pointed arrow pointing north, south, east, and west)</span></span><br/> |
| <span data-ttu-id="daa41-122">6</span><span class="sxs-lookup"><span data-stu-id="daa41-122">6</span></span><br/>  | <span data-ttu-id="daa41-123">No NE SW (двойная стрелка, указывающая на северо-восток и запад)</span><span class="sxs-lookup"><span data-stu-id="daa41-123">Size NE SW (double arrow pointing northeast and southwest)</span></span><br/>      |
| <span data-ttu-id="daa41-124">7</span><span class="sxs-lookup"><span data-stu-id="daa41-124">7</span></span><br/>  | <span data-ttu-id="daa41-125">Размер N S (двойная стрелка, указывающая на север и Юг)</span><span class="sxs-lookup"><span data-stu-id="daa41-125">Size N S (double arrow pointing north and south)</span></span><br/>                |
| <span data-ttu-id="daa41-126">8</span><span class="sxs-lookup"><span data-stu-id="daa41-126">8</span></span><br/>  | <span data-ttu-id="daa41-127">Размер NW, SE</span><span class="sxs-lookup"><span data-stu-id="daa41-127">Size NW, SE</span></span><br/>                                                     |
| <span data-ttu-id="daa41-128">9</span><span class="sxs-lookup"><span data-stu-id="daa41-128">9</span></span><br/>  | <span data-ttu-id="daa41-129">Размер E W (двойная стрелка, указывающая Восток и Западная)</span><span class="sxs-lookup"><span data-stu-id="daa41-129">Size E W (double arrow pointing east and west)</span></span><br/>                  |
| <span data-ttu-id="daa41-130">10</span><span class="sxs-lookup"><span data-stu-id="daa41-130">10</span></span><br/> | <span data-ttu-id="daa41-131">Стрелка вверх</span><span class="sxs-lookup"><span data-stu-id="daa41-131">Up Arrow</span></span><br/>                                                        |
| <span data-ttu-id="daa41-132">11</span><span class="sxs-lookup"><span data-stu-id="daa41-132">11</span></span><br/> | <span data-ttu-id="daa41-133">Песочные часы (ожидание)</span><span class="sxs-lookup"><span data-stu-id="daa41-133">Hourglass (wait)</span></span><br/>                                                |
| <span data-ttu-id="daa41-134">12</span><span class="sxs-lookup"><span data-stu-id="daa41-134">12</span></span><br/> | <span data-ttu-id="daa41-135">Без перетаскивания</span><span class="sxs-lookup"><span data-stu-id="daa41-135">No Drop</span></span><br/>                                                         |
| <span data-ttu-id="daa41-136">13</span><span class="sxs-lookup"><span data-stu-id="daa41-136">13</span></span><br/> | <span data-ttu-id="daa41-137">Стрелка и Песочные часы</span><span class="sxs-lookup"><span data-stu-id="daa41-137">Arrow and hourglass</span></span><br/>                                             |
| <span data-ttu-id="daa41-138">14</span><span class="sxs-lookup"><span data-stu-id="daa41-138">14</span></span><br/> | <span data-ttu-id="daa41-139">Стрелка и вопросительный знак</span><span class="sxs-lookup"><span data-stu-id="daa41-139">Arrow and question mark</span></span><br/>                                         |
| <span data-ttu-id="daa41-140">15</span><span class="sxs-lookup"><span data-stu-id="daa41-140">15</span></span><br/> | <span data-ttu-id="daa41-141">Изменить размер</span><span class="sxs-lookup"><span data-stu-id="daa41-141">Size all</span></span><br/>                                                        |
| <span data-ttu-id="daa41-142">99</span><span class="sxs-lookup"><span data-stu-id="daa41-142">99</span></span><br/> | <span data-ttu-id="daa41-143">Пользовательский значок, заданный свойством Маусеикон</span><span class="sxs-lookup"><span data-stu-id="daa41-143">Custom icon specified by the MouseIcon property</span></span><br/>                 |



 

## <a name="dispid_mouseicon"></a><span data-ttu-id="daa41-144">маусеикон DISPID \_</span><span class="sxs-lookup"><span data-stu-id="daa41-144">DISPID\_MOUSEICON</span></span>

<span data-ttu-id="daa41-145">Свойство типа изображения.</span><span class="sxs-lookup"><span data-stu-id="daa41-145">Property of type picture.</span></span>

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a><span data-ttu-id="daa41-146">изображение DISPID \_</span><span class="sxs-lookup"><span data-stu-id="daa41-146">DISPID\_PICTURE</span></span>

<span data-ttu-id="daa41-147">Свойство типа изображения.</span><span class="sxs-lookup"><span data-stu-id="daa41-147">Property of type picture.</span></span>

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a><span data-ttu-id="daa41-148">DISPID \_ допустим</span><span class="sxs-lookup"><span data-stu-id="daa41-148">DISPID\_VALID</span></span>

<span data-ttu-id="daa41-149">Используется для определения наличия в элементе управления допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="daa41-149">Used to determine if the control has valid data or not.</span></span>

<span data-ttu-id="daa41-150">Свойство типа BOOL.</span><span class="sxs-lookup"><span data-stu-id="daa41-150">Property of type BOOL.</span></span>

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a><span data-ttu-id="daa41-151">\_внешняя \_ ПАЛИТРа DISPID</span><span class="sxs-lookup"><span data-stu-id="daa41-151">DISPID\_ AMBIENT\_PALETTE</span></span>

<span data-ttu-id="daa41-152">Используется для того, чтобы элемент управления получил ХПАЛ контейнера.</span><span class="sxs-lookup"><span data-stu-id="daa41-152">Used to allow the control to get the container's HPAL.</span></span> <span data-ttu-id="daa41-153">Если контейнер предоставляет внешнюю палитру, то это единственная палитра, которая может быть реализована в переднем плане.</span><span class="sxs-lookup"><span data-stu-id="daa41-153">If the container supplies an ambient palette then that is the only palette that may be realized into the foreground.</span></span> <span data-ttu-id="daa41-154">Элементы управления, которые хотят реализовать собственные палитры, должны сделать это в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="daa41-154">Controls that want to realize their own palettes must do so in the background.</span></span> <span data-ttu-id="daa41-155">Если контейнер не содержит окружающей палитры, то активный элемент управления может реализовать свою палитру на переднем плане.</span><span class="sxs-lookup"><span data-stu-id="daa41-155">If there is no ambient palette provided by the container, then the active control can realize its palette in the foreground.</span></span> <span data-ttu-id="daa41-156">Обработка палитры обсуждается в разделе поведение палитры для элементов управления OLE, которые находятся в пакете SDK для ActiveX.</span><span class="sxs-lookup"><span data-stu-id="daa41-156">Palette handling is further discussed in Palette Behavior for OLE Controls which is in the ActiveX SDK.</span></span>

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





