---
title: О партнерстве
description: О партнерстве
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Проигрыватель Windows Media, партнерство
- Объектная модель проигрывателя Windows Media, партнерство
- Объектная модель, партнерство
- Элемент управления ActiveX проигрывателя Windows Media, партнерство
- Элемент управления ActiveX, партнерство
- Элемент управления ActiveX проигрывателя Windows Media Mobile, партнерство
- Проигрыватель Windows Media Mobile, партнерство
- синхронизация устройств, партнерство
- синхронизация устройств, партнерство
- партнерство между устройствами и проигрывателем Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104487284"
---
# <a name="about-partnerships"></a>О партнерстве

Партнерство — это специальная связь между портативным устройством и проигрывателем Windows Media. Пользователи могут установить связь с определенным устройством с помощью пользовательского интерфейса проигрывателя Windows Media. Можно программно управлять партнерством с помощью [ивмпсинкдевице:: креатепартнершип](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) и [Ивмпсинкдевице::d елетепартнершип](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership). Метод **креатепартнершип** запускает асинхронный процесс, который завершается, когда событие **креатепартнершипкомплете** получено через интерфейс **IWMPEvents2** .

Проигрыватель Windows Media 10 или более поздней версии поддерживает создание связей с до 16 устройств. У каждого партнерства есть связанный индекс партнерства. Индекс партнерства для конкретного устройства можно получить, вызвав [ивмпсинкдевице:: Get \_ партнершипиндекс](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex). Индексы партнерства нумеруются от 1 до 16. Если определенное устройство не имеет связи с проигрывателем Windows Media Player, **жетпартнершипиндекс** возвращает для индекса нулевое значение.

Состояние партнерства конкретного устройства можно получить, вызвав метод [ивмпсинкдевице:: Get \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) , а затем изменив полученное значение [вмпдевицестатус](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) . Проигрыватель Windows Media поддерживает одно партнерство с библиотекой одного пользователя на одном компьютере для каждого устройства. Это означает, что создание новой связи приведет к удалению любой существующей связи между текущим устройством и другим компьютером. Чтобы иметь представление об изменении состояния устройства, можно получить событие **девицестатусчанже** .

Проигрывателю Windows Media не удается создать связь с устройством с состоянием **вмпдсмануалдевице**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Сведения о синхронизации устройств**](about-device-synchronization.md)
</dt> <dt>

[**Интерфейс IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Работа с портативными устройствами**](working-with-portable-devices.md)
</dt> </dl>

 

 




