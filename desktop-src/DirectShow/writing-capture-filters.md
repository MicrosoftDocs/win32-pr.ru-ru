---
description: Запись фильтров записи
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Запись фильтров записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683623"
---
# <a name="writing-capture-filters"></a>Запись фильтров записи

Написание фильтра записи аудио или видео для DirectShow не рекомендуется. Вместо этого DirectShow обеспечивает автоматическую поддержку устройств видеозаписи аудио и видео, использование фильтров оболочки и [перечислителя системных устройств](system-device-enumerator.md). Дополнительные сведения о реализации драйвера устройства см. в документации по комплекту драйверов для Windows (WDK).

Этот раздел предназначен только для разработчиков, которым необходимо захватывать какие-либо пользовательские данные с необычного аппаратного устройства.

В этом разделе содержатся следующие подразделы:

-   [Требования к ПИН-коду для фильтров захвата](pin-requirements-for-capture-filters.md)
-   [Реализация предварительной версии ПИН-кода (необязательно)](implementing-a-preview-pin--optional.md)
-   [Создание данных в фильтре записи](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



