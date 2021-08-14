---
title: Клиентские API DVC
description: Клиентские API динамических виртуальных каналов (DVC) реализуются специально для клиента подключение к удаленному рабочему столу (RDC) подключения.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557f51adbf10562465f93a101e502632a791d5c272b278c5a8b7ea6124637913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130820"
---
# <a name="dvc-client-apis"></a>Клиентские API DVC

Клиентские API динамических виртуальных каналов (DVC) реализуются специально для клиента подключение к удаленному рабочему столу (RDC) подключения. Некоторые API реализуются платформой DVC, а некоторые реализуются разработчиком подключаемых модулей. Некоторые API-интерфейсы используются для поддержки подключаемого модуля клиента подключение к удаленному рабочему столу (RDC) и не связаны напрямую с транспортом данных.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Разрешает загрузку подключаемого модуля клиента подключение к удаленному рабочему столу (RDC) клиентом подключение к удаленному рабочему столу (RDC).

</dd> <dt>

[**ивтслистенер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Управляет параметрами конфигурации для каждого прослушивателя для подключения динамического виртуального канала (DVC).

</dd> <dt>

[**ивтслистенеркаллбакк**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Используется для уведомления подключаемого модуля клиента подключение к удаленному рабочему столу (RDC) о входящих запросах к определенному прослушивателю.

</dd> <dt>

[**ивтсвиртуалчаннелманажер**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Управляет всеми подключаемыми модулями клиента подключение к удаленному рабочему столу (RDC) и динамическими прослушивателями виртуальных каналов (DVC).

</dd> <dt>

[**ивтсвиртуалчаннел**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Используется для управления состоянием канала и записи в канале.

</dd> <dt>

[**ивтсвиртуалчаннелкаллбакк**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Получает уведомления об изменениях состояния канала или полученных данных.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Этот интерфейс не поддерживается.

</dd> <dt>

[**виртуалчаннелжетинстанце**](virtualchannelgetinstance.md)
</dt> <dd>

Вызывается для того, чтобы подключаемый модуль создает экземпляр интерфейса [**ивтсплугин**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) для всех подключаемых модулей, РЕАЛИЗОВАНных библиотекой DLL.

</dd> </dl>

 

 




