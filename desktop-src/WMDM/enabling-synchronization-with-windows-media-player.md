---
title: включение синхронизации с проигрыватель Windows Media
description: включение синхронизации с проигрыватель Windows Media
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows диспетчер устройств мультимедиа, синхронизация с проигрыватель Windows Media
- диспетчер устройств, синхронизация с проигрыватель Windows Media
- инструкции по программированию, синхронизация с проигрыватель Windows Media
- поставщики услуг, синхронизация с проигрыватель Windows Media
- создание поставщиков услуг, синхронизация с проигрыватель Windows Media
- синхронизация с проигрыватель Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef06dd0e32e0ea95674f54b94336ecb6882e8215775c857ee0780a58b71af75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585012"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>включение синхронизации с проигрыватель Windows Media

вы можете разрешить устройству участвовать в автоматической синхронизации с проигрыватель Windows Media. автоматическая синхронизация означает, что когда назначенное пользователем синхронизированное устройство подключается к компьютеру, проигрыватель Windows Media автоматически скачивает, обновляет или удаляет файлы с устройства, не требуя дополнительных входов пользователя.

по умолчанию следующие устройства синхронизируются с проигрыватель Windows Media:

-   Устройства MTP
-   Запоминающие устройства
-   устройства Windows CE (проигрыватель Windows Media 10 Mobile и более поздние версии)

для синхронизации любого другого устройства с проигрыватель Windows Media должны выполняться следующие требования.

-   Устройство должно объявлять интерфейс PAP-устройства {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}
-   Объекты устройства, возвращаемые поставщиком службы, должны поддерживать интерфейс **IMDSPDevice3** .
-   Параметру устройства Усикстендедвмдм должно быть присвоено значение **DWORD** , равное 1. Дополнительные сведения см. в разделе [Параметры устройства](device-parameters.md) .
-   Поставщик услуг должен реализовать следующие интерфейсы:

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Создание поставщика услуг**](creating-a-service-provider.md)
</dt> <dt>

[**Параметры устройства**](device-parameters.md)
</dt> </dl>

 

 




