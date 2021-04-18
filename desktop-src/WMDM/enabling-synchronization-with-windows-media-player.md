---
title: Включение синхронизации с проигрывателем Windows Media
description: Включение синхронизации с проигрывателем Windows Media
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Диспетчер устройств Windows Media, синхронизация с проигрывателем Windows Media
- Диспетчер устройств, синхронизация с проигрывателем Windows Media
- инструкции по программированию, синхронизация с проигрывателем Windows Media
- поставщики услуг, синхронизация с проигрывателем Windows Media
- Создание поставщиков услуг, синхронизация с проигрывателем Windows Media
- Синхронизация с проигрывателем Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691392"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Включение синхронизации с проигрывателем Windows Media

Вы можете разрешить устройству участвовать в автоматической синхронизации с помощью проигрывателя Windows Media. Автоматическая синхронизация означает, что когда назначенное пользователем Синхронизированное устройство подключается к компьютеру, проигрыватель Windows Media автоматически скачивает, обновляет или удаляет файлы с устройства, не требуя дополнительных входов пользователя.

По умолчанию следующие устройства синхронизируются с проигрывателем Windows Media.

-   Устройства MTP
-   Запоминающие устройства
-   Устройства Windows CE (проигрыватель Windows Media 10 Mobile и более поздние версии)

Для синхронизации любого другого устройства с проигрывателем Windows Media необходимо соблюдение следующих требований.

-   Устройство должно объявлять интерфейс PAP-устройства {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}
-   Объекты устройства, возвращаемые поставщиком службы, должны поддерживать интерфейс **IMDSPDevice3** .
-   Параметру устройства Усикстендедвмдм должно быть присвоено значение **DWORD** , равное 1. Дополнительные сведения см. в разделе [Параметры устройства](device-parameters.md) .
-   Поставщик услуг должен реализовать следующие интерфейсы:

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание поставщика услуг**](creating-a-service-provider.md)
</dt> <dt>

[**Параметры устройства**](device-parameters.md)
</dt> </dl>

 

 




