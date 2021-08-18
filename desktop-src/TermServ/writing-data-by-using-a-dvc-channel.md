---
title: Запись данных с помощью канала DVC
description: Запись данных канала с помощью динамического виртуального канала (DVC) является симметричным для сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов) и клиента.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e3f73b8e7a3d7db8ac109e84c9c638845af441b58568156782710fdac0968a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058251"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Запись данных с помощью канала DVC

Запись данных канала с помощью динамического виртуального канала (DVC) является симметричным для сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов) и клиента. Запись данных канала реализуется методом [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) интерфейса [**ивтсвиртуалчаннел**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .

На следующем рисунке показана отправка и получение пакета данных между клиентом и сервером DVC (подключаемым модулем DVC).

![Отправка и получение пакета данных между клиентом и сервером DVC](images/writedvcchannel.png)

 

 




