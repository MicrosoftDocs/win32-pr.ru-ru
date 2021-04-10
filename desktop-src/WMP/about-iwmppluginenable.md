---
title: О Ивмпплугиненабле
description: О Ивмпплугиненабле
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Подключаемые модули проигрывателя Windows Media, интерфейсы
- подключаемые модули, интерфейсы
- подключаемые модули обработки цифровых сигналов, интерфейсы
- Подключаемые модули DSP, интерфейсы
- интерфейсы, подключаемые модули DSP
- Подключаемые модули проигрывателя Windows Media, интерфейс Ивмпплугиненабле
- подключаемые модули, интерфейс Ивмпплугиненабле
- подключаемые модули обработки цифровых сигналов, интерфейс Ивмпплугиненабле
- Подключаемые модули DSP, интерфейс Ивмпплугиненабле
- Интерфейс Ивмпплугиненабле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986201"
---
# <a name="about-iwmppluginenable"></a><span data-ttu-id="a24a8-113">О Ивмпплугиненабле</span><span class="sxs-lookup"><span data-stu-id="a24a8-113">About IWMPPluginEnable</span></span>

<span data-ttu-id="a24a8-114">Для подключаемых модулей DSP в проигрывателе Windows Media требуется интерфейс **ивмпплугиненабле** . **Ивмпплугиненабле** содержит два метода, которые хранят, включил ли проигрыватель Windows Media подключаемый модуль DSP.</span><span class="sxs-lookup"><span data-stu-id="a24a8-114">The **IWMPPluginEnable** interface is required for Windows Media Player DSP plug-ins. **IWMPPluginEnable** contains two methods that store whether Windows Media Player has enabled the DSP plug-in.</span></span> <span data-ttu-id="a24a8-115">Проигрыватель Windows Media вызывает **ивмпплугиненабле:: SetEnable** при создании экземпляра подключаемого модуля DSP, передавая значение **true** , если он включил подключаемый модуль, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a24a8-115">Windows Media Player calls **IWMPPluginEnable::SetEnable** when it creates an instance of the DSP plug-in, passing a value of **TRUE** if it has enabled the plug-in or **FALSE** otherwise.</span></span>

<span data-ttu-id="a24a8-116">Подключаемые модули DSP могут оставаться загруженными, даже когда пользователь решает их отключить.</span><span class="sxs-lookup"><span data-stu-id="a24a8-116">DSP plug-ins may remain loaded even when the user chooses to disable them.</span></span> <span data-ttu-id="a24a8-117">Если этот параметр отключен, подключаемый модуль должен копировать данные из входного буфера в выходной буфер и выполнять только обработку преобразования формата, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="a24a8-117">When disabled, a plug-in must copy data from the input buffer to the output buffer, performing only format conversion processing, if applicable.</span></span>

<span data-ttu-id="a24a8-118">Проигрыватель Windows Media также вызывает этот метод до освобождения экземпляра подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="a24a8-118">Windows Media Player also calls this method before it releases an instance of the DSP plug-in.</span></span> <span data-ttu-id="a24a8-119">Это полезно, чтобы позволить клиентам подключаемого модуля проверить, включен ли в данный момент подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="a24a8-119">This is useful to allow clients of the plug-in to check whether the plug-in is currently enabled.</span></span> <span data-ttu-id="a24a8-120">Например, подключаемый модуль пользовательского интерфейса может изменить внешний вид элементов управления, чтобы предупредить пользователя о том, что подключаемый модуль DSP не подключен.</span><span class="sxs-lookup"><span data-stu-id="a24a8-120">For instance, a user interface plug-in might change the appearance of its controls to alert the user that the DSP plug-in is not connected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a24a8-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a24a8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a24a8-122">**Требуемые интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="a24a8-122">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




