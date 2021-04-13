---
title: Подключаемые интерфейсы DSP
description: Подключаемые интерфейсы DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP-интерфейсы
- Подключаемые модули проигрывателя Windows Media, интерфейсы
- подключаемые модули, DSP-интерфейсы
- подключаемые модули, интерфейсы
- подключаемые модули обработки цифровых сигналов, интерфейсы
- подключаемые модули обработки цифровых сигналов, интерфейс ИспеЦифипропертипаже
- Подключаемые модули DSP, интерфейсы
- Подключаемые модули DSP, интерфейс ИспеЦифипропертипаже
- интерфейсы, подключаемые модули DSP
- испеЦифипропертипаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "104412681"
---
# <a name="dsp-plug-in-interfaces"></a><span data-ttu-id="62ed1-113">Подключаемые интерфейсы DSP</span><span class="sxs-lookup"><span data-stu-id="62ed1-113">DSP Plug-in Interfaces</span></span>

<span data-ttu-id="62ed1-114">Интерфейсы подключаемых модулей обработки цифровых сигналов (DSP) используются для управления передачей данных между проигрывателем Windows Media и подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="62ed1-114">The digital signal processing (DSP) plug-in interfaces are used to manage data transfer between Windows Media Player and the plug-in.</span></span> <span data-ttu-id="62ed1-115">Все подключаемые модули DSP могут дополнительно реализовать интерфейс **испеЦифипропертипаже** для предоставления реализации страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="62ed1-115">All DSP plug-ins may optionally implement the **ISpecifyPropertyPage** interface to provide a property page implementation.</span></span>

<span data-ttu-id="62ed1-116">Для создания подключаемых модулей DSP требуются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="62ed1-116">The following interfaces are required for creating DSP plug-ins.</span></span>



| <span data-ttu-id="62ed1-117">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="62ed1-117">Interface</span></span>                                                | <span data-ttu-id="62ed1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="62ed1-118">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ed1-119">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="62ed1-119">**IMediaObject**</span></span>                                         | <span data-ttu-id="62ed1-120">Управляет обменом данными с помощью проигрывателя Windows Media и выполняет задачи по обработке цифровых сигналов.</span><span class="sxs-lookup"><span data-stu-id="62ed1-120">Manages data exchange with Windows Media Player and performs digital signal processing tasks.</span></span> <span data-ttu-id="62ed1-121">Подробная документация включена в пакет SDK для DirectX.</span><span class="sxs-lookup"><span data-stu-id="62ed1-121">Detailed documentation is included with the DirectX SDK.</span></span> |
| [<span data-ttu-id="62ed1-122">ивмпмедиаплугинрегистрар</span><span class="sxs-lookup"><span data-stu-id="62ed1-122">IWMPMediaPluginRegistrar</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | <span data-ttu-id="62ed1-123">Управляет регистрацией подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="62ed1-123">Manages plug-in registration.</span></span>                                                                                                                          |
| [<span data-ttu-id="62ed1-124">ивмпплугин</span><span class="sxs-lookup"><span data-stu-id="62ed1-124">IWMPPlugin</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | <span data-ttu-id="62ed1-125">Управляет подключением к проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="62ed1-125">Manages the connection to Windows Media Player.</span></span>                                                                                                        |
| [<span data-ttu-id="62ed1-126">ивмпплугиненабле</span><span class="sxs-lookup"><span data-stu-id="62ed1-126">IWMPPluginEnable</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | <span data-ttu-id="62ed1-127">Хранит, включен ли в данный момент подключаемый модуль Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="62ed1-127">Stores whether the plug-in is currently enabled by Windows Media Player.</span></span>                                                                               |
| [<span data-ttu-id="62ed1-128">ивмпсервицес</span><span class="sxs-lookup"><span data-stu-id="62ed1-128">IWMPServices</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | <span data-ttu-id="62ed1-129">Извлекает из проигрывателя сведения о текущем потоке времени и состоянии потока.</span><span class="sxs-lookup"><span data-stu-id="62ed1-129">Retrieves information from the Player about the current stream time and stream state.</span></span>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="62ed1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="62ed1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62ed1-131">**Справочник по программированию подключаемых модулей DSP**</span><span class="sxs-lookup"><span data-stu-id="62ed1-131">**DSP Plug-ins Programming Reference**</span></span>](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




