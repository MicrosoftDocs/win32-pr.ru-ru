---
title: Тип 1 подключаемый модуль интернет-магазина
description: Тип 1 подключаемый модуль интернет-магазина
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Интернет-магазины проигрывателя Windows Media, подключаемые модули
- Интернет-магазины, подключаемые модули
- Тип 1 Интернет-магазины, подключаемые модули
- Интернет-магазины проигрывателя Windows Media, интерфейс Ивмпконтентпартнер
- Интернет-магазины, интерфейс Ивмпконтентпартнер
- Тип 1 Интернет-магазины, интерфейс Ивмпконтентпартнер
- подключаемые модули, Интернет-магазины проигрывателя Windows Media
- подключаемые модули, Интернет-магазины
- подключаемые модули, тип 1 Интернет-магазины
- подключаемые модули, интерфейс Ивмпконтентпартнер
- Подключаемые модули проигрывателя Windows Media, введите 1 Интернет-магазины
- Подключаемые модули проигрывателя Windows Media, Интернет-магазины
- Подключаемые модули проигрывателя Windows Media, Интернет-магазины проигрывателя Windows Media
- Подключаемые модули проигрывателя Windows Media, интерфейс Ивмпконтентпартнер
- ивмпконтентпартнер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069704"
---
# <a name="type-1-online-store-plug-in"></a><span data-ttu-id="8161a-118">Тип 1 подключаемый модуль интернет-магазина</span><span class="sxs-lookup"><span data-stu-id="8161a-118">Type 1 Online Store Plug-in</span></span>

<span data-ttu-id="8161a-119">Чтобы воспользоваться преимуществами функций интеграции с библиотекой, необходимо создать подключаемый модуль, который реализует интерфейс [ивмпконтентпартнер](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) , с помощью поставщиков Интернет-магазинов типа 1.</span><span class="sxs-lookup"><span data-stu-id="8161a-119">To take advantage of library integration features, type 1 online store providers must create a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="8161a-120">Этот интерфейс предоставляет методы, которые проигрыватель Windows Media вызывает для уведомления Интернет-магазина о действиях, выполняемых проигрывателем, и получения конкретных сведений о содержимом Интернет-магазина, каталоге или самом хранилище.</span><span class="sxs-lookup"><span data-stu-id="8161a-120">This interface provides the methods that Windows Media Player calls to notify the online store about activities taking place in the Player and to retrieve specific information about online store content, the catalog, or the store itself.</span></span>

<span data-ttu-id="8161a-121">После того как проигрыватель Windows Media создаст экземпляр подключаемого модуля, игрок вызывает [ивмпконтентпартнер:: сеткаллбакк](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)и предоставляет указатель на интерфейс **ивмпконтентпартнеркаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="8161a-121">After Windows Media Player instantiates the plug-in, the Player calls [IWMPContentPartner::SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback), and provides a pointer to the **IWMPContentPartnerCallback** interface.</span></span> <span data-ttu-id="8161a-122">Этот интерфейс позволяет Интернет-магазину выполнять вызовы в проигрывателе Windows Media, чтобы предоставлять сведения о состоянии или инициировать определенные процессы, например загрузку музыкальной записи.</span><span class="sxs-lookup"><span data-stu-id="8161a-122">This interface gives the online store a way to make calls into Windows Media Player to provide status information or to initiate specific processes, such as downloading a music track.</span></span>

<span data-ttu-id="8161a-123">Проигрыватель Windows Media и подключаемый модуль запускаются в отдельных процессах.</span><span class="sxs-lookup"><span data-stu-id="8161a-123">Windows Media Player and the plug-in run in separate processes.</span></span> <span data-ttu-id="8161a-124">Подключаемый модуль — это внутрипроцессный сервер, работающий в заданном по умолчанию суррогате DLL, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="8161a-124">The plug-in is an in-process server that runs in the default DLL surrogate, dllhost.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8161a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8161a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8161a-126">**Сведения об Интернет-магазинах типа 1**</span><span class="sxs-lookup"><span data-stu-id="8161a-126">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8161a-127">**Интерфейс Ивмпконтентпартнер**</span><span class="sxs-lookup"><span data-stu-id="8161a-127">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[<span data-ttu-id="8161a-128">**Интерфейс Ивмпконтентпартнеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="8161a-128">**IWMPContentPartnerCallback Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




