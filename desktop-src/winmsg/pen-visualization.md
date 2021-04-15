---
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении одного из перечисленных жестов пера.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Визуализация пера (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545575"
---
# <a name="pen-visualization"></a><span data-ttu-id="e92b9-103">Визуализация пера</span><span class="sxs-lookup"><span data-stu-id="e92b9-103">Pen Visualization</span></span>

<span data-ttu-id="e92b9-104">Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении одного из перечисленных жестов пера.</span><span class="sxs-lookup"><span data-stu-id="e92b9-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed pen gestures is detected.</span></span>

<span data-ttu-id="e92b9-105">Эти константы используются с параметрами **SPI \_ Жетпенвисуализатион** и **SPI \_ сетпенвисуализатион** и функцией [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e92b9-105">These constants are used with the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="e92b9-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**ПЕНВИСУАЛИЗАТИОН \_**</span><span class="sxs-lookup"><span data-stu-id="e92b9-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e92b9-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="e92b9-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="e92b9-108">Указывает, что обратная связь пользовательского интерфейса для всех жестов пера отключена.</span><span class="sxs-lookup"><span data-stu-id="e92b9-108">Specifies that UI feedback for all pen gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e92b9-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**ПЕНВИСУАЛИЗАТИОН \_**</span><span class="sxs-lookup"><span data-stu-id="e92b9-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e92b9-110">0x0023</span><span class="sxs-lookup"><span data-stu-id="e92b9-110">0x0023</span></span>
</dt> <dt>



<span data-ttu-id="e92b9-111">Указывает, что для всех жестов пера включена обратная связь пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e92b9-111">Specifies that UI feedback for all pen gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e92b9-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**ПЕНВИСУАЛИЗАТИОН \_ коснуться**</span><span class="sxs-lookup"><span data-stu-id="e92b9-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e92b9-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="e92b9-113">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="e92b9-114">Указывает отзыв пользовательского интерфейса для касания пером.</span><span class="sxs-lookup"><span data-stu-id="e92b9-114">Specifies UI feedback for a pen tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e92b9-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**ПЕНВИСУАЛИЗАТИОН \_ даублетап**</span><span class="sxs-lookup"><span data-stu-id="e92b9-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e92b9-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="e92b9-116">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="e92b9-117">Указывает отзыв пользовательского интерфейса для двойного касания пером.</span><span class="sxs-lookup"><span data-stu-id="e92b9-117">Specifies UI feedback for a pen double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e92b9-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**ПЕНВИСУАЛИЗАТИОН \_ курсор**</span><span class="sxs-lookup"><span data-stu-id="e92b9-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION\_CURSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e92b9-119">0x0020</span><span class="sxs-lookup"><span data-stu-id="e92b9-119">0x0020</span></span>
</dt> <dt>



<span data-ttu-id="e92b9-120">Указывает отзыв пользовательского интерфейса для курсора пера.</span><span class="sxs-lookup"><span data-stu-id="e92b9-120">Specifies UI feedback for the pen cursor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e92b9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e92b9-121">Requirements</span></span>



| <span data-ttu-id="e92b9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e92b9-122">Requirement</span></span> | <span data-ttu-id="e92b9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e92b9-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e92b9-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e92b9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e92b9-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e92b9-125">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e92b9-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e92b9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e92b9-127">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e92b9-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e92b9-128">Header</span><span class="sxs-lookup"><span data-stu-id="e92b9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e92b9-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e92b9-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e92b9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e92b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e92b9-131">Константы конфигурации</span><span class="sxs-lookup"><span data-stu-id="e92b9-131">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="e92b9-132">**Связь с визуализацией**</span><span class="sxs-lookup"><span data-stu-id="e92b9-132">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="e92b9-133">**системпараметерсинфо**</span><span class="sxs-lookup"><span data-stu-id="e92b9-133">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="e92b9-134">Настройка обратной связи для ввода</span><span class="sxs-lookup"><span data-stu-id="e92b9-134">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

