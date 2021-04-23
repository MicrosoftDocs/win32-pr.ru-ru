---
title: Клиентские API DVC
description: Клиентские API динамических виртуальных каналов (DVC) реализуются специально для клиента подключение к удаленному рабочему столу (RDC) подключения.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329483"
---
# <a name="dvc-client-apis"></a><span data-ttu-id="73d98-103">Клиентские API DVC</span><span class="sxs-lookup"><span data-stu-id="73d98-103">DVC Client APIs</span></span>

<span data-ttu-id="73d98-104">Клиентские API динамических виртуальных каналов (DVC) реализуются специально для клиента подключение к удаленному рабочему столу (RDC) подключения.</span><span class="sxs-lookup"><span data-stu-id="73d98-104">The dynamic virtual channel (DVC) client APIs are implemented specifically for the Remote Desktop Connection (RDC) client of the connection.</span></span> <span data-ttu-id="73d98-105">Некоторые API реализуются платформой DVC, а некоторые реализуются разработчиком подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="73d98-105">Some of the APIs are implemented by the DVC framework, and some are implemented by the plug-in developer.</span></span> <span data-ttu-id="73d98-106">Некоторые API-интерфейсы используются для поддержки подключаемого модуля клиента подключение к удаленному рабочему столу (RDC) и не связаны напрямую с транспортом данных.</span><span class="sxs-lookup"><span data-stu-id="73d98-106">Some of the APIs are used to support the Remote Desktop Connection (RDC) client plug-in, and are not directly related to data transport.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="73d98-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="73d98-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="73d98-108">**ивтсплугин**</span><span class="sxs-lookup"><span data-stu-id="73d98-108">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

<span data-ttu-id="73d98-109">Разрешает загрузку подключаемого модуля клиента подключение к удаленному рабочему столу (RDC) клиентом подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="73d98-109">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="73d98-110">**ивтслистенер**</span><span class="sxs-lookup"><span data-stu-id="73d98-110">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

<span data-ttu-id="73d98-111">Управляет параметрами конфигурации для каждого прослушивателя для подключения динамического виртуального канала (DVC).</span><span class="sxs-lookup"><span data-stu-id="73d98-111">Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.</span></span>

</dd> <dt>

[<span data-ttu-id="73d98-112">**ивтслистенеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="73d98-112">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

<span data-ttu-id="73d98-113">Используется для уведомления подключаемого модуля клиента подключение к удаленному рабочему столу (RDC) о входящих запросах к определенному прослушивателю.</span><span class="sxs-lookup"><span data-stu-id="73d98-113">Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span>

</dd> <dt>

[<span data-ttu-id="73d98-114">**ивтсвиртуалчаннелманажер**</span><span class="sxs-lookup"><span data-stu-id="73d98-114">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

<span data-ttu-id="73d98-115">Управляет всеми подключаемыми модулями клиента подключение к удаленному рабочему столу (RDC) и динамическими прослушивателями виртуальных каналов (DVC).</span><span class="sxs-lookup"><span data-stu-id="73d98-115">Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners.</span></span>

</dd> <dt>

[<span data-ttu-id="73d98-116">**ивтсвиртуалчаннел**</span><span class="sxs-lookup"><span data-stu-id="73d98-116">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

<span data-ttu-id="73d98-117">Используется для управления состоянием канала и записи в канале.</span><span class="sxs-lookup"><span data-stu-id="73d98-117">Used to control the channel state, and writes on the channel.</span></span>

</dd> <dt>

[<span data-ttu-id="73d98-118">**ивтсвиртуалчаннелкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="73d98-118">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

<span data-ttu-id="73d98-119">Получает уведомления об изменениях состояния канала или полученных данных.</span><span class="sxs-lookup"><span data-stu-id="73d98-119">Receives notifications about channel state changes or data received.</span></span>

</dd> <dt>

[<span data-ttu-id="73d98-120">**IWTSVirtualChannelCallback2**</span><span class="sxs-lookup"><span data-stu-id="73d98-120">**IWTSVirtualChannelCallback2**</span></span>](iwtsvirtualchannelcallback2.md)
</dt> <dd>

<span data-ttu-id="73d98-121">Этот интерфейс не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="73d98-121">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="73d98-122">**виртуалчаннелжетинстанце**</span><span class="sxs-lookup"><span data-stu-id="73d98-122">**VirtualChannelGetInstance**</span></span>](virtualchannelgetinstance.md)
</dt> <dd>

<span data-ttu-id="73d98-123">Вызывается для того, чтобы подключаемый модуль создает экземпляр интерфейса [**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) для всех подключаемых модулей, РЕАЛИЗОВАНных библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="73d98-123">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

</dd> </dl>

 

 




