---
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении входного контакта.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Визуализация контакта (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348192"
---
# <a name="contact-visualization"></a><span data-ttu-id="ebbb7-103">Связь с визуализацией</span><span class="sxs-lookup"><span data-stu-id="ebbb7-103">Contact Visualization</span></span>

<span data-ttu-id="ebbb7-104">Следующие константы используются приложениями или платформами пользовательского интерфейса для определения того, как обрабатывается обратная связь пользовательского интерфейса при обнаружении входного контакта.</span><span class="sxs-lookup"><span data-stu-id="ebbb7-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when an input contact is detected.</span></span>

<span data-ttu-id="ebbb7-105">Эти константы используются с параметрами **SPI \_ Жетконтактвисуализатион** и **SPI \_ сетконтактвисуализатион** и функцией [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ebbb7-105">These constants are used with the **SPI\_GETCONTACTVISUALIZATION** and **SPI\_SETCONTACTVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="ebbb7-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**КОНТАКТВИСУАЛИЗАТИОН \_**</span><span class="sxs-lookup"><span data-stu-id="ebbb7-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebbb7-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="ebbb7-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="ebbb7-108">Указывает, что отзывы о пользовательском интерфейсе для всех контактов отключены.</span><span class="sxs-lookup"><span data-stu-id="ebbb7-108">Specifies UI feedback for all contacts is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebbb7-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**КОНТАКТВИСУАЛИЗАТИОН \_**</span><span class="sxs-lookup"><span data-stu-id="ebbb7-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebbb7-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="ebbb7-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="ebbb7-111">Указывает Отзывы о пользовательском интерфейсе для всех контактов.</span><span class="sxs-lookup"><span data-stu-id="ebbb7-111">Specifies UI feedback for all contacts is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebbb7-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**КОНТАКТВИСУАЛИЗАТИОН \_ пресентатионмоде**</span><span class="sxs-lookup"><span data-stu-id="ebbb7-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION\_PRESENTATIONMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebbb7-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="ebbb7-113">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="ebbb7-114">Указывает Отзывы о пользовательском интерфейсе для всех контактов с визуальными элементами режима представления.</span><span class="sxs-lookup"><span data-stu-id="ebbb7-114">Specifies UI feedback for all contacts is on with presentation mode visuals.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebbb7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ebbb7-115">Requirements</span></span>



| <span data-ttu-id="ebbb7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ebbb7-116">Requirement</span></span> | <span data-ttu-id="ebbb7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ebbb7-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ebbb7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebbb7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ebbb7-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ebbb7-119">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ebbb7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebbb7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ebbb7-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ebbb7-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ebbb7-122">Header</span><span class="sxs-lookup"><span data-stu-id="ebbb7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebbb7-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebbb7-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebbb7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebbb7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbb7-125">Константы конфигурации</span><span class="sxs-lookup"><span data-stu-id="ebbb7-125">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="ebbb7-126">**Визуализация жестов**</span><span class="sxs-lookup"><span data-stu-id="ebbb7-126">**Gesture Visualization**</span></span>](gesture-visualization.md)
</dt> <dt>

[<span data-ttu-id="ebbb7-127">**системпараметерсинфо**</span><span class="sxs-lookup"><span data-stu-id="ebbb7-127">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="ebbb7-128">Настройка обратной связи для ввода</span><span class="sxs-lookup"><span data-stu-id="ebbb7-128">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

