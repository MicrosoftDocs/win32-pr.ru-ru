---
title: Запуск прослушивателя DVC
description: Чтобы установить успешное подключение между двумя модулями динамических виртуальных каналов (DVC), работающими на клиенте подключение к удаленному рабочему столу (RDC), необходимо запустить прослушиватель DVC и в состоянии прослушивания.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d440069cb64597c16a14323a67926376bf1c425f5a29c77e451c52866a5399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000454"
---
# <a name="starting-a-dvc-listener"></a>Запуск прослушивателя DVC

Чтобы установить успешное подключение между двумя модулями динамических виртуальных каналов (DVC), работающими на клиенте подключение к удаленному рабочему столу (RDC), необходимо запустить прослушиватель DVC и в состоянии прослушивания.

Создание экземпляра прослушивателя обычно происходит в методе [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) подключаемого модуля DVC. Однако создание экземпляров не ограничивается методом **Initialize** и может быть запущено в любой точке выполнения подключаемого модуля. Прослушиватель описывается интерфейсом [**ивтслистенер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) , который создается экземпляром [**ивтсвиртуалчаннелманажер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Экземпляр диспетчера каналов передается в подключаемый модуль в точке инициализации. Подключаемый модуль может поддерживать внутреннюю ссылку на экземпляр, если это необходимо.

Подключаемый модуль может создавать экземпляры всех прослушивателей по мере необходимости. Любое входящее подключение будет обрабатываться [**ивтслистенеркаллбакк**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), который предоставляется в методе [**креателистенер**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) [**ивтсвиртуалчаннелманажер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Пример см. в описании реализации **кдвксамплеплугин:: Initialize** в примере кода [подключаемого модуля клиента DVC](dvc-client-plug-in-example.md) .

 

 




