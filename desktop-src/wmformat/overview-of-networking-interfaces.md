---
title: Обзор сетевых интерфейсов
description: Обзор сетевых интерфейсов
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Пакет SDK для формата мультимедиа, сетевые интерфейсы
- Windows Пакет SDK для формата мультимедиа, интерфейсы
- Расширенный системный формат (ASF), сетевые интерфейсы
- ASF (Расширенный системный формат), сетевые интерфейсы
- Расширенный системный формат (ASF), список интерфейсов для сетевых функций
- ASF (Расширенный системный формат), список интерфейсов для сетевых функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b87da220f5ac61b7b722e79939a1fd617af46ab6608d4d92e8905f466bb98e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700266"
---
# <a name="overview-of-networking-interfaces"></a>Обзор сетевых интерфейсов

Сетевые возможности этого пакета SDK поддерживаются с помощью методов следующих интерфейсов.



| Интерфейс                                                  | Описание                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ивмклиентконнектионс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | Возвращает сведения о клиентах, подключенных к сетевому приемнику.                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | Предоставляет метод для получения сведений о клиенте, подключенном к приемнику сети записи. Этот интерфейс расширяет интерфейс **ивмклиентконнектионс** . |
| [**ивмкредентиалкаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | Предоставляет метод обратного вызова для получения учетных данных пользователя при доступе к удаленному сайту.                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | Предоставляет дополнительные методы для объекта Reader.                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | Расширяет интерфейс **IWMReaderAdvanced2** .                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | Расширяет интерфейс **IWMReaderAdvanced3** .                                                                                                         |
| [**ивмреадернетворкконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | Настраивает параметры сети для объекта модуля чтения.                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | Настраивает дополнительные параметры сети для объекта Reader. Этот интерфейс расширяет интерфейс **ивмреадернетворкконфиг** .                         |
| [**ивмвритернетворксинк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | Настраивает объект сетевого приемника, который используется для записи цифрового мультимедиа в сеть.                                                                |
| [**ивмвритерпушсинк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | Настраивает объект приемника push-уведомлений, который используется для распространения цифровых носителей в точки публикации.                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Реализация функций сети**](implementing-network-functionality.md)
</dt> </dl>

 

 




