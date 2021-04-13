---
title: Обновления мастера подключаемых модулей DSP для проигрывателя Windows Media 11
description: Обновления мастера подключаемых модулей DSP для проигрывателя Windows Media 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Подключаемые модули проигрывателя Windows Media, мастер подключаемых модулей
- подключаемые модули, мастер подключаемых модулей
- подключаемые модули обработки цифровых сигналов, мастер подключаемых модулей
- Подключаемые модули DSP, мастер подключаемых модулей
- Мастер подключаемых модулей
- Visual Studio, мастер подключаемых модулей DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412520"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a><span data-ttu-id="f9a9b-109">Обновления мастера подключаемых модулей DSP для проигрывателя Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="f9a9b-109">Updates to the DSP Plug-in Wizard for Windows Media Player 11</span></span>

<span data-ttu-id="f9a9b-110">В пакете SDK для проигрывателя Windows Media 11 представлены следующие изменения в мастере подключаемых модулей DSP.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-110">The Windows Media Player 11 SDK introduces the following changes to the DSP plug-in wizard:</span></span>

-   <span data-ttu-id="f9a9b-111">Подключаемые модули регистрируют модель потоков как "оба".</span><span class="sxs-lookup"><span data-stu-id="f9a9b-111">Plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="f9a9b-112">Это позволяет запустить подключаемый модуль в конвейере Media Foundation в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-112">This enables the plug-in to run in the Media Foundation pipeline on Windows Vista.</span></span> <span data-ttu-id="f9a9b-113">Ознакомьтесь с файлом *имяПроекта*. RGS.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-113">See the *projectname*.rgs file.</span></span>

    -   <span data-ttu-id="f9a9b-114">Подключаемые модули DSP аудиоподсистемы поддерживают следующие два дополнительных формата:</span><span class="sxs-lookup"><span data-stu-id="f9a9b-114">Audio DSP plug-ins have support for the following two additional formats:</span></span>

    <!-- -->

    -   <span data-ttu-id="f9a9b-115">\_Формат волны \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="f9a9b-115">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
    -   <span data-ttu-id="f9a9b-116">\_Формат Wave \_ , расширяемый с подформатом КСДАТАФОРМАТ \_ подтипа \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-116">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

    <span data-ttu-id="f9a9b-117">См. файл *имя_проекта*. cpp.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-117">See the *projectname*.cpp file.</span></span>

    1.  <span data-ttu-id="f9a9b-118">Подключаемые модули DSP видео поддерживают формат видео NV12.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-118">Video DSP plug-ins have support for the NV12 video format.</span></span>
    2.  <span data-ttu-id="f9a9b-119">Подключаемые модули выполняют дополнительные вызовы [ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) и [Ивмпмедиаплугинрегистрар:: вмпунрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) с новым типом подключаемого модуля: WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-119">Plug-ins make additional calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC.</span></span> <span data-ttu-id="f9a9b-120">См. файл *прожектнамедлл*. cpp проекта.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-120">See the project's *projectnamedll*.cpp file.</span></span>
    3.  <span data-ttu-id="f9a9b-121">Дополнительный проект в каждом решении создает прокси-или заглушку библиотеки DLL для настраиваемого интерфейса параметров страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-121">An additional project in each solution creates a proxy/stub DLL for the property page settings custom interface.</span></span> <span data-ttu-id="f9a9b-122">См. проект *прожектнамепс* .</span><span class="sxs-lookup"><span data-stu-id="f9a9b-122">See the *projectnamePS* project.</span></span>
    4.  <span data-ttu-id="f9a9b-123">Вызовы устаревших методов были изменены для использования последних версий.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-123">Calls to deprecated methods have been changed to use the newest versions.</span></span>
    5.  <span data-ttu-id="f9a9b-124">Мастер может создать подключаемый модуль двойного режима, который работает как DMO, реализовав **имедиаобжект** и как MFT, реализовав **имфтрансформ**.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-124">The wizard can generate a dual-mode plug-in that functions both as a DMO, by implementing **IMediaObject**, and as an MFT, by implementing **IMFTransform**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9a9b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f9a9b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9a9b-126">**Мастер подключаемых модулей DSP**</span><span class="sxs-lookup"><span data-stu-id="f9a9b-126">**DSP Plug-in Wizard**</span></span>](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




