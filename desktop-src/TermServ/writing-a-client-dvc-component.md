---
title: Написание клиентского модуля DVC
description: Чтобы создать клиентский модуль динамического виртуального канала (DVC), сначала необходимо реализовать и зарегистрировать подключаемый модуль клиента подключение к удаленному рабочему столу (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681471"
---
# <a name="writing-a-client-dvc-module"></a><span data-ttu-id="9b3f6-103">Написание клиентского модуля DVC</span><span class="sxs-lookup"><span data-stu-id="9b3f6-103">Writing a Client DVC Module</span></span>

<span data-ttu-id="9b3f6-104">Чтобы создать клиентский модуль динамического виртуального канала (DVC), сначала необходимо реализовать и зарегистрировать подключаемый модуль клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="9b3f6-104">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span> <span data-ttu-id="9b3f6-105">Подключаемый модуль DVC — это реализация [**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), зарегистрированная как объект модели COM.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-105">The DVC plug-in is an implementation of [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registered as a Component Object Model (COM) object.</span></span>

> [!Note]  
> <span data-ttu-id="9b3f6-106">Подключаемый модуль должен быть реализован в модели произвольной потоковой обработки.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-106">The plug-in must be implemented in a free-threading model.</span></span> <span data-ttu-id="9b3f6-107">Реализация модели-контейнера не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-107">Apartment-model implementation is not supported.</span></span>

 

<span data-ttu-id="9b3f6-108">Ниже приведен список интерфейсов, которые реализуются объектами, экземплярами которых является подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-108">The following is a list of interfaces that are implemented by objects that are instantiated by the plug-in.</span></span>



| <span data-ttu-id="9b3f6-109">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="9b3f6-109">Interface</span></span>                                                        | <span data-ttu-id="9b3f6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9b3f6-110">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b3f6-111">**ивтсплугин**</span><span class="sxs-lookup"><span data-stu-id="9b3f6-111">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | <span data-ttu-id="9b3f6-112">Разрешает загрузку подключаемого модуля клиента подключение к удаленному рабочему столу (RDC) клиентом подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="9b3f6-112">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span><br/>                                                                 |
| [<span data-ttu-id="9b3f6-113">**ивтслистенеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9b3f6-113">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | <span data-ttu-id="9b3f6-114">Уведомляет клиентский подключаемый модуль подключение к удаленному рабочему столу (RDC) о входящих запросах к определенному прослушивателю.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-114">Notifies the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span><br/>                                                                             |
| [<span data-ttu-id="9b3f6-115">**ивтсвиртуалчаннелкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9b3f6-115">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | <span data-ttu-id="9b3f6-116">Получает уведомления об изменениях состояния канала или полученных данных.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-116">Receives notifications about channel state changes or data received.</span></span> <span data-ttu-id="9b3f6-117">Каждый экземпляр этого интерфейса связан с одним экземпляром [**ивтсвиртуалчаннел**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span><span class="sxs-lookup"><span data-stu-id="9b3f6-117">Each instance of this interface is associated with one instance of [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span></span><br/> |



 

<span data-ttu-id="9b3f6-118">Ниже приведен список интерфейсов, которые реализуются объектами, созданными с помощью клиента подключение к удаленному рабочему столу (RDC), и являются частью платформы.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-118">The following is a list of interfaces that are implemented by objects that are instantiated by the Remote Desktop Connection (RDC) client, and are part of the framework.</span></span>



| <span data-ttu-id="9b3f6-119">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="9b3f6-119">Interface</span></span>                                                      | <span data-ttu-id="9b3f6-120">Описание</span><span class="sxs-lookup"><span data-stu-id="9b3f6-120">Description</span></span>                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b3f6-121">**ивтсвиртуалчаннелманажер**</span><span class="sxs-lookup"><span data-stu-id="9b3f6-121">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | <span data-ttu-id="9b3f6-122">Управляет всеми подключаемыми модулями клиента подключение к удаленному рабочему столу (RDC), прослушивателями DVC или статическими виртуальными каналами.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-122">Manages all Remote Desktop Connection (RDC) client plug-ins, DVC listeners, or static virtual channels.</span></span><br/> |
| [<span data-ttu-id="9b3f6-123">**ивтслистенер**</span><span class="sxs-lookup"><span data-stu-id="9b3f6-123">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | <span data-ttu-id="9b3f6-124">Управляет параметрами конфигурации для каждого прослушивателя для подключения DVC.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-124">Manages configuration settings for each listener for the DVC connection.</span></span><br/>                                |
| [<span data-ttu-id="9b3f6-125">**ивтсвиртуалчаннел**</span><span class="sxs-lookup"><span data-stu-id="9b3f6-125">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | <span data-ttu-id="9b3f6-126">Управляет состоянием канала, а также записью в канале.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-126">Controls the channel state, as well as writes on the channel.</span></span><br/>                                           |



 

<span data-ttu-id="9b3f6-127">На следующем рисунке показана связь между клиентом подключение к удаленному рабочему столу (RDC) и подключаемым модулем клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="9b3f6-127">The following illustration shows the relationship between the Remote Desktop Connection (RDC) client and the Remote Desktop Connection (RDC) client plug-in.</span></span>

![связь между клиентом и подключаемым модулем](images/tsclient.png)

 

 





