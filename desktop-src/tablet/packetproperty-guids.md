---
description: В следующей таблице перечислены идентификаторы GUID свойств пакетов, используемые в \_ структуре свойств пакета.
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: Идентификаторы GUID Паккетпроперти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913547"
---
# <a name="packetproperty-guids"></a><span data-ttu-id="b01ba-103">Идентификаторы GUID Паккетпроперти</span><span class="sxs-lookup"><span data-stu-id="b01ba-103">PacketProperty GUIDs</span></span>

<span data-ttu-id="b01ba-104">В следующей таблице перечислены идентификаторы GUID свойств пакетов, используемые в структуре [**\_ свойств пакета**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .</span><span class="sxs-lookup"><span data-stu-id="b01ba-104">The following table lists packet property GUIDs used by the [**PACKET\_PROPERTY**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b01ba-105">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="b01ba-105">GUID</span></span></th>
<th><span data-ttu-id="b01ba-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b01ba-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b01ba-107">GUID_ALTITUDE_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="b01ba-107">GUID_ALTITUDE_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="b01ba-108">Угол между осью пера и поверхностью планшета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-108">Angle between the axis of the pen and the surface of the tablet.</span></span> <span data-ttu-id="b01ba-109">Значение равно 0, если перо находится рядом с поверхностью и 90, когда перо расположено перпендикулярно поверхности.</span><span class="sxs-lookup"><span data-stu-id="b01ba-109">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span> <span data-ttu-id="b01ba-110">При инвертировании пера значения становятся отрицательными.</span><span class="sxs-lookup"><span data-stu-id="b01ba-110">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b01ba-111">GUID_AZIMUTH_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="b01ba-111">GUID_AZIMUTH_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="b01ba-112">Поворот курсора вокруг оси z по часовой стрелке через полный круговой диапазон.</span><span class="sxs-lookup"><span data-stu-id="b01ba-112">Clockwise rotation of the cursor around the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b01ba-113">GUID_BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="b01ba-113">GUID_BOXNUMBER</span></span><br/></td>
<td><span data-ttu-id="b01ba-114">Идентификатор GUID, используемый для получения номера рамки для распознавания рукописного ввода, если распознаватель работает в текстовом режиме.</span><span class="sxs-lookup"><span data-stu-id="b01ba-114">The GUID that is used to retrieve the box number for an ink recognition alternate when the recognizer is operating in box mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b01ba-115">GUID_BUTTON_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="b01ba-115">GUID_BUTTON_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="b01ba-116">Давление нажатия на кнопку с учетом нажима.</span><span class="sxs-lookup"><span data-stu-id="b01ba-116">Pressure on a pressure-sensitive button.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b01ba-117">GUID_NORMAL_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="b01ba-117">GUID_NORMAL_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="b01ba-118">Идентификатор GUID для объекта Паккетпроперти, который представляет давление кончика пера перпендикулярно поверхности планшета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-118">The GUID for the PacketProperty object that represents pressure of the pen tip perpendicular to the tablet surface.</span></span> <span data-ttu-id="b01ba-119">Чем больше нажим на кончик пера, тем больше чернил рисуется.</span><span class="sxs-lookup"><span data-stu-id="b01ba-119">The greater the pressure put on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b01ba-120">GUID_PACKET_STATUS</span><span class="sxs-lookup"><span data-stu-id="b01ba-120">GUID_PACKET_STATUS</span></span><br/></td>
<td><span data-ttu-id="b01ba-121">Содержит одно или несколько следующих значений флагов:</span><span class="sxs-lookup"><span data-stu-id="b01ba-121">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="b01ba-122">Курсор касается поверхности рисования (значение = 1).</span><span class="sxs-lookup"><span data-stu-id="b01ba-122">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="b01ba-123">Курсор инвертирован.</span><span class="sxs-lookup"><span data-stu-id="b01ba-123">The cursor is inverted.</span></span> <span data-ttu-id="b01ba-124">Например, конец пера указывает на поверхность (значение = 2).</span><span class="sxs-lookup"><span data-stu-id="b01ba-124">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="b01ba-125">Не используется (значение = 4).</span><span class="sxs-lookup"><span data-stu-id="b01ba-125">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="b01ba-126">Нажата кнопка пера (Value = 8).</span><span class="sxs-lookup"><span data-stu-id="b01ba-126">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b01ba-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span><span class="sxs-lookup"><span data-stu-id="b01ba-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span></span><br/></td>
<td><span data-ttu-id="b01ba-128">Идентификатор контакта устройства для пакета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-128">The device contact identifier for a packet.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b01ba-129">GUID_SERIAL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="b01ba-129">GUID_SERIAL_NUMBER</span></span><br/></td>
<td><span data-ttu-id="b01ba-130">Определяет пакет.</span><span class="sxs-lookup"><span data-stu-id="b01ba-130">Identifies the packet.</span></span> <span data-ttu-id="b01ba-131">Это то же значение, которое используется для получения пакета из очереди пакетов.</span><span class="sxs-lookup"><span data-stu-id="b01ba-131">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b01ba-132">GUID_TANGENT_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="b01ba-132">GUID_TANGENT_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="b01ba-133">Идентификатор GUID для объекта Паккетпроперти, который представляет давление кончика пера вдоль плоскости планшета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-133">The GUID for the PacketProperty object that represents pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b01ba-134">GUID_TIMER_TICK</span><span class="sxs-lookup"><span data-stu-id="b01ba-134">GUID_TIMER_TICK</span></span><br/></td>
<td><span data-ttu-id="b01ba-135">Время создания пакета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-135">Time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b01ba-136">GUID_TWIST_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="b01ba-136">GUID_TWIST_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="b01ba-137">Поворот курсора по часовой стрелке вокруг своей собственной оси.</span><span class="sxs-lookup"><span data-stu-id="b01ba-137">Clockwise rotation of the cursor around its own axis.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b01ba-138">GUID_X</span><span class="sxs-lookup"><span data-stu-id="b01ba-138">GUID_X</span></span><br/></td>
<td><span data-ttu-id="b01ba-139">Координата x в пространстве координат планшета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-139">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="b01ba-140">Каждый пакет содержит это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b01ba-140">Each packet contains this property by default.</span></span> <span data-ttu-id="b01ba-141">Источник (0, 0) планшета — левый верхний угол.</span><span class="sxs-lookup"><span data-stu-id="b01ba-141">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b01ba-142">GUID_X_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="b01ba-142">GUID_X_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="b01ba-143">Для курсора пера ориентация x-наклона — это угол между осью y, z, а также плоскостью пера и оси y.</span><span class="sxs-lookup"><span data-stu-id="b01ba-143">For a pen cursor, the x-tilt orientation is the angle between the y,z-plane and the pen and y-axis plane.</span></span> <span data-ttu-id="b01ba-144">Значение равно 0, если перо расположено перпендикулярно области рисования и положительное, когда перо находится справа от перпендикулярного.</span><span class="sxs-lookup"><span data-stu-id="b01ba-144">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b01ba-145">GUID_Y</span><span class="sxs-lookup"><span data-stu-id="b01ba-145">GUID_Y</span></span><br/></td>
<td><span data-ttu-id="b01ba-146">Координата y в пространстве координат планшета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-146">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="b01ba-147">Каждый пакет содержит это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b01ba-147">Each packet contains this property by default.</span></span> <span data-ttu-id="b01ba-148">Источник (0, 0) планшета — левый верхний угол.</span><span class="sxs-lookup"><span data-stu-id="b01ba-148">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b01ba-149">GUID_Y_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="b01ba-149">GUID_Y_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="b01ba-150">Для курсора пера ориентация наклона по оси y — это угол между осью x, z и плоскостью пера и оси x.</span><span class="sxs-lookup"><span data-stu-id="b01ba-150">For a pen cursor, the y-tilt orientation is the angle between the x,z-plane and the pen and x-axis plane.</span></span> <span data-ttu-id="b01ba-151">Значение равно 0, когда перо расположено перпендикулярно поверхности рисования и положительно, когда перо перемещается или выходит за пределы пользователя.</span><span class="sxs-lookup"><span data-stu-id="b01ba-151">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward, or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b01ba-152">GUID_Z</span><span class="sxs-lookup"><span data-stu-id="b01ba-152">GUID_Z</span></span><br/></td>
<td><span data-ttu-id="b01ba-153">Z-координата или расстояние от кончика пера с поверхности планшета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-153">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="b01ba-154">Тип перечисления <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> определяет единицу измерения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b01ba-154">The <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> enumeration type determines the unit of measurement for this property.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="b01ba-155">Поле Танжентпрессуре представляет давление на плоскости поверхности планшета; поле Нормалпрессуре представляет давление, перпендикулярное плоскости поверхности планшета.</span><span class="sxs-lookup"><span data-stu-id="b01ba-155">The TangentPressure field represents pressure along the plane of the tablet surface; the NormalPressure field represents pressure perpendicular to the plane of the tablet surface.</span></span>

 

 

 




