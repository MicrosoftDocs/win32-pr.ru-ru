---
title: Принятие подключения (службы удаленных рабочих столов)
description: В некоторый момент времени клиент динамического виртуального канала (DVC) запрашивает подключение к прослушивателю DVC.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104556018"
---
# <a name="accepting-a-connection-remote-desktop-services"></a><span data-ttu-id="7073f-103">Принятие подключения (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="7073f-103">Accepting a Connection (Remote Desktop Services)</span></span>

<span data-ttu-id="7073f-104">В некоторый момент времени клиент динамического виртуального канала (DVC) запрашивает подключение к прослушивателю DVC.</span><span class="sxs-lookup"><span data-stu-id="7073f-104">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span> <span data-ttu-id="7073f-105">В этом случае прослушиватель может создать уникальный коммуникационный канал для клиента, который обрабатывается методом [**Онневчаннелконнектион**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) [**ивтслистенеркаллбакк**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span><span class="sxs-lookup"><span data-stu-id="7073f-105">When this occurs, the listener can spawn a unique communication channel to the client, which is handled by the [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) method of [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span></span> <span data-ttu-id="7073f-106">Пример см. в описании реализации **кдвксамплеплугин:: онневчаннелконнектион** в примере кода [подключаемого модуля клиента DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="7073f-106">For an example, see the implementation of **CDVCSamplePlugin::OnNewChannelConnection** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

<span data-ttu-id="7073f-107">На следующем рисунке показана последовательность событий для установления соединения DVC.</span><span class="sxs-lookup"><span data-stu-id="7073f-107">The following figure shows the sequence of events for establishing a DVC connection.</span></span> <span data-ttu-id="7073f-108">Затененные объекты предоставляются пользователем (DVC Application/Service и [**ивтслистенеркаллбакк**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), а незатененные объекты являются частью платформы (удаленный рабочий стол узла сеансов (узел сеансов удаленных рабочих столов), прослушиватель и [**ивтсвиртуалчаннел**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span><span class="sxs-lookup"><span data-stu-id="7073f-108">The shaded objects are user-supplied (DVC application/service and [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), while the un-shaded objects are part of the framework (Remote Desktop Session Host (RD Session Host) service, listener, and [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span></span>

![последовательность событий для установления соединения DVC](images/acceptingconnection.png)

> [!Note]  
> <span data-ttu-id="7073f-110">На этом рисунке предполагается, что объект прослушивателя был создан с помощью вызова [**креателистенер**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) в [**ивтсвиртуалчаннелманажер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)и что подключаемый модуль указал [**ивтслистенеркаллбакк**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="7073f-110">This figure assumes that a listener object has been created through a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) call to [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), and that the plug-in has specified [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) as a parameter.</span></span>

 

 

 




