---
title: Запуск прослушивателя DVC
description: Чтобы установить успешное подключение между двумя модулями динамических виртуальных каналов (DVC), работающими на клиенте подключение к удаленному рабочему столу (RDC), необходимо запустить прослушиватель DVC и в состоянии прослушивания.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332387"
---
# <a name="starting-a-dvc-listener"></a><span data-ttu-id="14596-103">Запуск прослушивателя DVC</span><span class="sxs-lookup"><span data-stu-id="14596-103">Starting a DVC Listener</span></span>

<span data-ttu-id="14596-104">Чтобы установить успешное подключение между двумя модулями динамических виртуальных каналов (DVC), работающими на клиенте подключение к удаленному рабочему столу (RDC), необходимо запустить прослушиватель DVC и в состоянии прослушивания.</span><span class="sxs-lookup"><span data-stu-id="14596-104">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

<span data-ttu-id="14596-105">Создание экземпляра прослушивателя обычно происходит в методе [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) подключаемого модуля DVC.</span><span class="sxs-lookup"><span data-stu-id="14596-105">The instantiation of a listener typically occurs in the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of the DVC plug-in.</span></span> <span data-ttu-id="14596-106">Однако создание экземпляров не ограничивается методом **Initialize** и может быть запущено в любой точке выполнения подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="14596-106">However, instantiation is not limited to the **Initialize** method, and can be started at any point of the plug-in execution.</span></span> <span data-ttu-id="14596-107">Прослушиватель описывается интерфейсом [**ивтслистенер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) , который создается экземпляром [**ивтсвиртуалчаннелманажер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="14596-107">The listener is described by the [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) interface which is instantiated by the [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="14596-108">Экземпляр диспетчера каналов передается в подключаемый модуль в точке инициализации.</span><span class="sxs-lookup"><span data-stu-id="14596-108">An instance to the channel manager is passed to the plug-in at the initialization point.</span></span> <span data-ttu-id="14596-109">Подключаемый модуль может поддерживать внутреннюю ссылку на экземпляр, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="14596-109">The plug-in can maintain an internal reference to the instance as long as it needs to.</span></span>

<span data-ttu-id="14596-110">Подключаемый модуль может создавать экземпляры всех прослушивателей по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="14596-110">A plug-in can instantiate as many listeners as it needs to.</span></span> <span data-ttu-id="14596-111">Любое входящее подключение будет обрабатываться [**ивтслистенеркаллбакк**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), который предоставляется в методе [**креателистенер**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) [**ивтсвиртуалчаннелманажер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="14596-111">Any incoming connection will be handled by [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), which is supplied in the [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) method of [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="14596-112">Пример см. в описании реализации **кдвксамплеплугин:: Initialize** в примере кода [подключаемого модуля клиента DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="14596-112">For an example, see the implementation of **CDVCSamplePlugin::Initialize** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

 

 




