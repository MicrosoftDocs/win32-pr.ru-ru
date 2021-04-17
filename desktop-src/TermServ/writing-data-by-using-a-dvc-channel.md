---
title: Запись данных с помощью канала DVC
description: Запись данных канала с помощью динамического виртуального канала (DVC) является симметричным для сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов) и клиента.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681470"
---
# <a name="writing-data-by-using-a-dvc-channel"></a><span data-ttu-id="2d9e7-103">Запись данных с помощью канала DVC</span><span class="sxs-lookup"><span data-stu-id="2d9e7-103">Writing Data by Using a DVC Channel</span></span>

<span data-ttu-id="2d9e7-104">Запись данных канала с помощью динамического виртуального канала (DVC) является симметричным для сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов) и клиента.</span><span class="sxs-lookup"><span data-stu-id="2d9e7-104">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span> <span data-ttu-id="2d9e7-105">Запись данных канала реализуется методом [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) интерфейса [**ивтсвиртуалчаннел**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .</span><span class="sxs-lookup"><span data-stu-id="2d9e7-105">The writing of channel data is implemented by the [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) method of the [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) interface.</span></span>

<span data-ttu-id="2d9e7-106">На следующем рисунке показана отправка и получение пакета данных между клиентом и сервером DVC (подключаемым модулем DVC).</span><span class="sxs-lookup"><span data-stu-id="2d9e7-106">The following illustration shows the sending and receiving of the data packet between the DVC client and server (DVC plug-in).</span></span>

![Отправка и получение пакета данных между клиентом и сервером DVC](images/writedvcchannel.png)

 

 




