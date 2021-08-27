---
description: Запись фильтров записи
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Запись фильтров записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa4807f381dc925a68fa3c60e45d5c8c5c444653230f366895b370e97aaccb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049094"
---
# <a name="writing-capture-filters"></a>Запись фильтров записи

не рекомендуется писать звуковой файл или фильтр захвата видео для DirectShow. вместо этого DirectShow обеспечивает автоматическую поддержку устройств видеозаписи аудио и видео, использование фильтров оболочки и [перечислителя системных устройств](system-device-enumerator.md). дополнительные сведения о реализации драйвера устройства см. в документации по Windows driver Kit (WDK).

Этот раздел предназначен только для разработчиков, которым необходимо захватывать какие-либо пользовательские данные с необычного аппаратного устройства.

В этом разделе содержатся следующие подразделы:

-   [Требования к ПИН-коду для фильтров захвата](pin-requirements-for-capture-filters.md)
-   [Реализация предварительной версии ПИН-кода (необязательно)](implementing-a-preview-pin--optional.md)
-   [Создание данных в фильтре записи](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



