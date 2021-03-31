---
description: Определяет значения, указывающие свойства пакета.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Константы Паккетпропертигуидс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272623"
---
# <a name="packetpropertyguids-constants"></a><span data-ttu-id="61a95-103">Константы Паккетпропертигуидс</span><span class="sxs-lookup"><span data-stu-id="61a95-103">PacketPropertyGuids Constants</span></span>

<span data-ttu-id="61a95-104">Определяет значения, указывающие свойства пакета.</span><span class="sxs-lookup"><span data-stu-id="61a95-104">Defines values that specify the packet properties.</span></span> <span data-ttu-id="61a95-105">В планшетном ПКАПИ используются идентификаторы GUID для идентификации свойств пакетов, которые в COM являются константными строками.</span><span class="sxs-lookup"><span data-stu-id="61a95-105">The Tablet PCAPI uses globally unique identifiers (GUIDs) to identify packet properties, which in COM are constant strings.</span></span>

<span data-ttu-id="61a95-106">В C++ вы можете получить доступ к этим константам в файле заголовка Мсинкаут. h, который находится в папке <systemdrive> : \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ include, если пакет SDK установлен в расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61a95-106">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span> <span data-ttu-id="61a95-107">В C++ эти константы являются Вчарс, а не BSTRs.</span><span class="sxs-lookup"><span data-stu-id="61a95-107">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="61a95-108">Преобразуйте их в BSTRs перед использованием.</span><span class="sxs-lookup"><span data-stu-id="61a95-108">Convert them into BSTRs before use.</span></span> <span data-ttu-id="61a95-109">Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="61a95-109">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

<span data-ttu-id="61a95-110">В следующей таблице перечислены доступные поля свойств пакетов с глобальным уникальным идентификатором (GUID).</span><span class="sxs-lookup"><span data-stu-id="61a95-110">The following table lists the available packet property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="61a95-111">Используйте эти идентификаторы GUID, чтобы указать, какие свойства пакет содержит при создании контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="61a95-111">Use these GUIDs to specify which properties the packet contains when you create the tablet context.</span></span> <span data-ttu-id="61a95-112">Чтобы определить диапазон и разрешение свойства, вызовите метод [**жетпропертиметрикс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) .</span><span class="sxs-lookup"><span data-stu-id="61a95-112">To determine the range and resolution of a property, call the [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) method.</span></span> <span data-ttu-id="61a95-113">Константы в таблице ниже, начиная с "STR \_ ", представляют собой строковые представления соответствующих двоичных констант, показанных в той же ячейке таблицы.</span><span class="sxs-lookup"><span data-stu-id="61a95-113">The constants in the table below beginning with "STR\_" are string representations of the corresponding binary constants shown in the same table cell.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="61a95-114">Константа</span><span class="sxs-lookup"><span data-stu-id="61a95-114">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="61a95-115">Описание</span><span class="sxs-lookup"><span data-stu-id="61a95-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <span data-ttu-id="61a95-116"><dt><strong>STR_GUID_X или GUID_PACKETPROPERTY_GUID_X</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-116"><dt><strong>STR_GUID_X or GUID_PACKETPROPERTY_GUID_X</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-117">Координата x в пространстве координат планшета.</span><span class="sxs-lookup"><span data-stu-id="61a95-117">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="61a95-118">Каждый пакет содержит это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61a95-118">Each packet contains this property by default.</span></span> <span data-ttu-id="61a95-119">Источник (0, 0) планшета — левый верхний угол.</span><span class="sxs-lookup"><span data-stu-id="61a95-119">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="61a95-120"><dt><strong>STR_GUID_Y или GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-120"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-121">Координата y в пространстве координат планшета.</span><span class="sxs-lookup"><span data-stu-id="61a95-121">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="61a95-122">Каждый пакет содержит это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61a95-122">Each packet contains this property by default.</span></span> <span data-ttu-id="61a95-123">Источник (0, 0) планшета — левый верхний угол.</span><span class="sxs-lookup"><span data-stu-id="61a95-123">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="61a95-124"><dt><strong>STR_GUID_Y или GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-124"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-125">Координата y в пространстве координат планшета.</span><span class="sxs-lookup"><span data-stu-id="61a95-125">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="61a95-126">Каждый пакет содержит это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61a95-126">Each packet contains this property by default.</span></span> <span data-ttu-id="61a95-127">Источник (0, 0) планшета — левый верхний угол.</span><span class="sxs-lookup"><span data-stu-id="61a95-127">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <span data-ttu-id="61a95-128"><dt><strong>STR_GUID_Z или GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-128"><dt><strong>STR_GUID_Z or GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-129">Z-координата или расстояние от кончика пера с поверхности планшета.</span><span class="sxs-lookup"><span data-stu-id="61a95-129">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="61a95-130">Тип перечисления <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>таблетпропертиметрикунит</strong></a> определяет единицу измерения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="61a95-130">The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> enumeration type determines the unit of measurement for this property.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <span data-ttu-id="61a95-131"><dt><strong>STR_GUID_PAKETSTATUS или GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-131"><dt><strong>STR_GUID_PAKETSTATUS or GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-132">Содержит одно или несколько следующих значений флагов:</span><span class="sxs-lookup"><span data-stu-id="61a95-132">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="61a95-133">Курсор касается поверхности рисования (значение = 1).</span><span class="sxs-lookup"><span data-stu-id="61a95-133">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="61a95-134">Курсор инвертирован.</span><span class="sxs-lookup"><span data-stu-id="61a95-134">The cursor is inverted.</span></span> <span data-ttu-id="61a95-135">Например, конец пера указывает на поверхность (значение = 2).</span><span class="sxs-lookup"><span data-stu-id="61a95-135">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="61a95-136">Не используется (значение = 4).</span><span class="sxs-lookup"><span data-stu-id="61a95-136">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="61a95-137">Нажата кнопка пера (Value = 8).</span><span class="sxs-lookup"><span data-stu-id="61a95-137">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="61a95-138"><dt><strong>STR_GUID_TIMERTICK или GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-138"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-139">Время создания пакета.</span><span class="sxs-lookup"><span data-stu-id="61a95-139">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="61a95-140"><dt><strong>STR_GUID_TIMERTICK или GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-140"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-141">Время создания пакета.</span><span class="sxs-lookup"><span data-stu-id="61a95-141">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <span data-ttu-id="61a95-142"><dt><strong>STR_GUID_SERIALNUMBER или GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-142"><dt><strong>STR_GUID_SERIALNUMBER or GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-143">Свойство пакета для идентификации пакета.</span><span class="sxs-lookup"><span data-stu-id="61a95-143">The packet property for identifying the packet.</span></span><br/> <span data-ttu-id="61a95-144">Это то же значение, которое используется для получения пакета из очереди пакетов.</span><span class="sxs-lookup"><span data-stu-id="61a95-144">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <span data-ttu-id="61a95-145"><dt><strong>STR_GUID_NORMALPRESSURE или GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-145"><dt><strong>STR_GUID_NORMALPRESSURE or GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-146">Давление кончика пера перпендикулярно поверхности планшета.</span><span class="sxs-lookup"><span data-stu-id="61a95-146">The pressure of the pen tip perpendicular to the tablet surface.</span></span><br/> <span data-ttu-id="61a95-147">Чем больше нажим на кончик пера, тем больше чернил рисуется.</span><span class="sxs-lookup"><span data-stu-id="61a95-147">The greater the pressure on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <span data-ttu-id="61a95-148"><dt><strong>STR_GUID_TANGENTPRESSURE или GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-148"><dt><strong>STR_GUID_TANGENTPRESSURE or GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-149">Давление кончика пера вдоль плоскости планшета.</span><span class="sxs-lookup"><span data-stu-id="61a95-149">The pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <span data-ttu-id="61a95-150"><dt><strong>STR_GUID_BUTTONPRESSURE или GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-150"><dt><strong>STR_GUID_BUTTONPRESSURE or GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-151">Давление нажатия на кнопку с учетом нажима.</span><span class="sxs-lookup"><span data-stu-id="61a95-151">The pressure on a pressure sensitive button.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <span data-ttu-id="61a95-152"><dt><strong>STR_GUID_XTILTORIENTATION или GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-152"><dt><strong>STR_GUID_XTILTORIENTATION or GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-153">Угол между y, z-плоскостью и плоскостью пера и оси y.</span><span class="sxs-lookup"><span data-stu-id="61a95-153">The angle between the y,z-plane and the pen and y-axis plane.</span></span><br/> <span data-ttu-id="61a95-154">Применяется к курсору пера.</span><span class="sxs-lookup"><span data-stu-id="61a95-154">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="61a95-155">Значение равно 0, если перо расположено перпендикулярно области рисования и положительное, когда перо находится справа от перпендикулярного.</span><span class="sxs-lookup"><span data-stu-id="61a95-155">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <span data-ttu-id="61a95-156"><dt><strong>STR_GUID_YTILTORIENTATION или GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-156"><dt><strong>STR_GUID_YTILTORIENTATION or GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-157">Угол между плоскостью x, z и плоскостью пера и оси x.</span><span class="sxs-lookup"><span data-stu-id="61a95-157">The angle between the x,z-plane and the pen and x-axis plane.</span></span><br/> <span data-ttu-id="61a95-158">Применяется к курсору пера.</span><span class="sxs-lookup"><span data-stu-id="61a95-158">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="61a95-159">Значение равно 0, когда перо расположено перпендикулярно поверхности рисования и положительно, когда перо перемещается от пользователя вверх или вниз.</span><span class="sxs-lookup"><span data-stu-id="61a95-159">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <span data-ttu-id="61a95-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION или GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION or GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-161">Поворот курсора относительно оси z по часовой стрелке через полный круговой диапазон.</span><span class="sxs-lookup"><span data-stu-id="61a95-161">The clockwise rotation of the cursor about the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <span data-ttu-id="61a95-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION или GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION or GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-163">Угол между осью пера и поверхностью планшета.</span><span class="sxs-lookup"><span data-stu-id="61a95-163">The angle between the axis of the pen and the surface of the tablet.</span></span><br/> <span data-ttu-id="61a95-164">Значение равно 0, если перо находится рядом с поверхностью и 90, когда перо расположено перпендикулярно поверхности.</span><span class="sxs-lookup"><span data-stu-id="61a95-164">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span><br/> <span data-ttu-id="61a95-165">При инвертировании пера значения становятся отрицательными.</span><span class="sxs-lookup"><span data-stu-id="61a95-165">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <span data-ttu-id="61a95-166"><dt><strong>STR_GUID_TWISTORIENTATION или GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-166"><dt><strong>STR_GUID_TWISTORIENTATION or GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-167">Поворот курсора по часовой стрелке относительно своей собственной оси.</span><span class="sxs-lookup"><span data-stu-id="61a95-167">The clockwise rotation of the cursor about its own axis.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <span data-ttu-id="61a95-168"><dt><strong>STR_GUID_PITCHROTATION или GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-168"><dt><strong>STR_GUID_PITCHROTATION or GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-169">Свойство Packet, которое указывает, находится ли tip над горизонтальной линией или под ней, перпендикулярной поверхности письма.</span><span class="sxs-lookup"><span data-stu-id="61a95-169">The packet property that indicates whether the tip is above or below a horizontal line that is perpendicular to the writing surface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="61a95-170">Для этого требуется трехмерный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="61a95-170">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="61a95-171">Значение является положительным, если Совет находится над линией, и отрицательно, если он находится ниже строки.</span><span class="sxs-lookup"><span data-stu-id="61a95-171">The value is positive if the tip is above the line and negative if it is below the line.</span></span> <span data-ttu-id="61a95-172">Например, если вы держите перо перед вами и пишете на мнимой стене, то этот шаг будет положительным, если Совет находится над линией, переданной на стену.</span><span class="sxs-lookup"><span data-stu-id="61a95-172">For example, if you hold the pen in front of you and write on an imaginary wall, the pitch is positive if the tip is above a line extending from you to the wall.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <span data-ttu-id="61a95-173"><dt><strong>STR_GUID_ROLLROTATION или GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-173"><dt><strong>STR_GUID_ROLLROTATION or GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-174">Поворот пера по часовой стрелке вокруг его собственной оси.</span><span class="sxs-lookup"><span data-stu-id="61a95-174">The clockwise rotation of the pen around its own axis.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="61a95-175">Для этого требуется трехмерный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="61a95-175">This requires a 3D digitizer.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="61a95-176"><dt><strong>STR_GUID_YAWROTATION или GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-176"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-177">Угол пера слева или справа от центра его горизонтальной оси, когда перо горизонтально.</span><span class="sxs-lookup"><span data-stu-id="61a95-177">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="61a95-178">Для этого требуется трехмерный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="61a95-178">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="61a95-179">Если вы удерживаете перо перед вами и пишете на мнимой стене, ноль значения нутации указывает, что перо перпендикулярно стене.</span><span class="sxs-lookup"><span data-stu-id="61a95-179">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="61a95-180">Значение является отрицательным, если TIP расположен слева от перпендикулярного и положительного, если TIP расположен справа от перпендикулярного.</span><span class="sxs-lookup"><span data-stu-id="61a95-180">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="61a95-181"><dt><strong>STR_GUID_YAWROTATION или GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-181"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-182">Угол пера слева или справа от центра его горизонтальной оси, когда перо горизонтально.</span><span class="sxs-lookup"><span data-stu-id="61a95-182">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="61a95-183">Для этого требуется трехмерный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="61a95-183">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="61a95-184">Если вы удерживаете перо перед вами и пишете на мнимой стене, ноль значения нутации указывает, что перо перпендикулярно стене.</span><span class="sxs-lookup"><span data-stu-id="61a95-184">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="61a95-185">Значение является отрицательным, если TIP расположен слева от перпендикулярного и положительного, если TIP расположен справа от перпендикулярного.</span><span class="sxs-lookup"><span data-stu-id="61a95-185">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <span data-ttu-id="61a95-186"><dt><strong>STR_GUID_WIDTH или GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-186"><dt><strong>STR_GUID_WIDTH or GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-187">Ширина области контакта в сенсорном дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="61a95-187">The width of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <span data-ttu-id="61a95-188"><dt><strong>STR_GUID_HEIGHT или GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-188"><dt><strong>STR_GUID_HEIGHT or GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-189">Высота контактной зоны на сенсорном дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="61a95-189">The height of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <span data-ttu-id="61a95-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE или GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE or GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-191">Уровень достоверности пальца в сенсорном дигитайзере.</span><span class="sxs-lookup"><span data-stu-id="61a95-191">The level of confidence that there was finger contact on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <span data-ttu-id="61a95-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID или GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="61a95-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID or GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="61a95-193">Идентификатор контакта устройства для пакета.</span><span class="sxs-lookup"><span data-stu-id="61a95-193">The device contact identifier for a packet.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="61a95-194">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61a95-194">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="61a95-195">Все значения пакетов, поступающие от оборудования планшета, являются целыми числами размером 32 бит.</span><span class="sxs-lookup"><span data-stu-id="61a95-195">All packet values coming from the tablet hardware are 32-bit size integers.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61a95-196">Требования</span><span class="sxs-lookup"><span data-stu-id="61a95-196">Requirements</span></span>



| <span data-ttu-id="61a95-197">Требование</span><span class="sxs-lookup"><span data-stu-id="61a95-197">Requirement</span></span> | <span data-ttu-id="61a95-198">Значение</span><span class="sxs-lookup"><span data-stu-id="61a95-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a95-199">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61a95-199">Minimum supported client</span></span><br/> | <span data-ttu-id="61a95-200">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="61a95-200">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="61a95-201">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61a95-201">Minimum supported server</span></span><br/> | <span data-ttu-id="61a95-202">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="61a95-202">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="61a95-203">Header</span><span class="sxs-lookup"><span data-stu-id="61a95-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="61a95-204"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="61a95-204"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61a95-205">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61a95-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a95-206">**Метод Испаккетпропертисуппортед**</span><span class="sxs-lookup"><span data-stu-id="61a95-206">**IsPacketPropertySupported Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[<span data-ttu-id="61a95-207">**Метод Жетпропертиметрикс**</span><span class="sxs-lookup"><span data-stu-id="61a95-207">**GetPropertyMetrics Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[<span data-ttu-id="61a95-208">**Интерфейс Иинктаблет**</span><span class="sxs-lookup"><span data-stu-id="61a95-208">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




