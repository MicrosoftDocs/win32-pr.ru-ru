---
title: Управление размером пакетов
description: Управление размером пакетов
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media Format SDK, управление размерами пакетов
- Windows Media Format SDK, размеры пакетов
- профили, размеры пакетов
- профили, Управление размером пакетов
- пакеты, размеры
- пакеты, интерфейс Ивмпаккетсизе
- ивмпаккетсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412698"
---
# <a name="managing-packet-size"></a>Управление размером пакетов

Модуль записи предназначен для внутреннего управления размером пакетов. Однако у вас могут быть особые требования к приложению, которые вызывают ручное управление размером пакетов в файлах ASF, которые вы пишете. Windows Media Format SDK предоставляет два интерфейса, [**ивмпаккетсизе**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) и [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , которые позволяют управлять максимальным и минимальным размером пакетов.

Оба интерфейса размера пакета представлены в объекте Profile. Они также доступны для объекта Reader. Как и в случае с другими интерфейсами, связанными с профилями, читатель может обращаться только к методам чтения.

Размер пакетов оказывает некоторое воздействие на производительность. Как правило, чем меньше размер пакета, тем более фрагментированными являются данные в файле. Чем сложнее Фрагментирование файла, тем менее эффективным будет его перестроение. В сценарии потоковой передачи это может не быть важным фактором, поскольку процесс чтения файла из источника в Интернете обычно неэффективен. Тем не менее, при работе с файлом локально это может быть важно.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпаккетсизе**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**Интерфейс IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Работа с профилями**](working-with-profiles.md)
</dt> </dl>

 

 




