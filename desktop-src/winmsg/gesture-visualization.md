---
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении одного из указанных жестов.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Визуализация жестов (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693507"
---
# <a name="gesture-visualization"></a><span data-ttu-id="1f7d4-103">Визуализация жестов</span><span class="sxs-lookup"><span data-stu-id="1f7d4-103">Gesture Visualization</span></span>

<span data-ttu-id="1f7d4-104">Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении одного из указанных жестов.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed gestures is detected.</span></span>

<span data-ttu-id="1f7d4-105">Эти константы используются с параметрами **SPI \_ Жетжестуревисуализатион** и **SPI \_ сетжестуревисуализатион** и функцией [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="1f7d4-105">These constants are used with the **SPI\_GETGESTUREVISUALIZATION** and **SPI\_SETGESTUREVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="1f7d4-106">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-106">**Note**</span></span>  

<span data-ttu-id="1f7d4-107">Для получения или установки сведений о визуализации пера рекомендуется использовать параметры **SPI \_ Жетпенвисуализатион** и **SPI \_ сетпенвисуализатион** , а также константы, перечисленные в поле [**визуализация пера**](pen-visualization.md).</span><span class="sxs-lookup"><span data-stu-id="1f7d4-107">For retrieving or setting pen visualization info, we recommend that you use the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the constants listed in [**Pen Visualization**](pen-visualization.md).</span></span>

<dl> <dt>

<span data-ttu-id="1f7d4-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7d4-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="1f7d4-109">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="1f7d4-110">Указывает, что обратная связь пользовательского интерфейса для всех жестов отключена.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-110">Specifies that UI feedback for all gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f7d4-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7d4-112">0x001F</span><span class="sxs-lookup"><span data-stu-id="1f7d4-112">0x001F</span></span>
</dt> <dt>



<span data-ttu-id="1f7d4-113">Указывает, что для всех жестов включена обратная связь пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-113">Specifies that UI feedback for all gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f7d4-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ коснуться**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7d4-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="1f7d4-115">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="1f7d4-116">Указывает отзыв пользовательского интерфейса для касания.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-116">Specifies UI feedback for a tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f7d4-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ даублетап**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7d4-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="1f7d4-118">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="1f7d4-119">Указывает отзыв пользовательского интерфейса для двойного касания.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-119">Specifies UI feedback for a double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f7d4-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ прессандтап**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION\_PRESSANDTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7d4-121">0x0004</span><span class="sxs-lookup"><span data-stu-id="1f7d4-121">0x0004</span></span>
</dt> <dt>



<span data-ttu-id="1f7d4-122">Указывает отзыв пользовательского интерфейса для нажатия и касания.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-122">Specifies UI feedback for a press and tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f7d4-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ прессандхолд**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION\_PRESSANDHOLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7d4-124">0x0008</span><span class="sxs-lookup"><span data-stu-id="1f7d4-124">0x0008</span></span>
</dt> <dt>



<span data-ttu-id="1f7d4-125">Указывает отзыв пользовательского интерфейса для нажатия и удерживания.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-125">Specifies UI feedback for a press and hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f7d4-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**ЖЕСТУРЕВИСУАЛИЗАТИОН \_ ригхттап**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION\_RIGHTTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f7d4-127">0x0010</span><span class="sxs-lookup"><span data-stu-id="1f7d4-127">0x0010</span></span>
</dt> <dt>



<span data-ttu-id="1f7d4-128">Указывает отзыв пользовательского интерфейса для правильного касания.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-128">Specifies UI feedback for a right tap.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f7d4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1f7d4-129">Requirements</span></span>



| <span data-ttu-id="1f7d4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1f7d4-130">Requirement</span></span> | <span data-ttu-id="1f7d4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1f7d4-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7d4-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f7d4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7d4-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f7d4-133">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1f7d4-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f7d4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7d4-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1f7d4-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1f7d4-136">Header</span><span class="sxs-lookup"><span data-stu-id="1f7d4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f7d4-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f7d4-137"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f7d4-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f7d4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7d4-139">Константы конфигурации</span><span class="sxs-lookup"><span data-stu-id="1f7d4-139">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="1f7d4-140">**Связь с визуализацией**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-140">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="1f7d4-141">**системпараметерсинфо**</span><span class="sxs-lookup"><span data-stu-id="1f7d4-141">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="1f7d4-142">Настройка обратной связи для ввода</span><span class="sxs-lookup"><span data-stu-id="1f7d4-142">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

