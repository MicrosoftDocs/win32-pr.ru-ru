---
description: WMI использует трассировку событий (ETW) и события можно получить с помощью пользовательского интерфейса Просмотр событий или программы командной строки wevtutil. Дополнительные сведения см. в разделе Трассировка действия WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Файлы журналов WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fff9064dd82484568282f649b3380f544d9ba58a569e36583664806d47b5e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739431"
---
# <a name="wmi-log-files"></a>Файлы журналов WMI

WMI использует [трассировку событий](/windows/desktop/ETW/event-tracing-portal) (ETW) и события можно получить с помощью пользовательского интерфейса **Просмотр событий** или программы командной строки wevtutil. Дополнительные сведения см. в разделе [Трассировка действия WMI](tracing-wmi-activity.md).

-   [Трассировка событий вместо текстовых журналов](#event-tracing-instead-of-text-logs)
-   [Файлы журналов WMI](#wmi-log-files)
-   [Связанные темы](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Трассировка событий вместо текстовых журналов

Действия службы WMI записываются в файл ВмитраЦинг. log. Дополнительные сведения о включении трассировки событий WMI и обращении к файлу ВмитраЦинг. log см. в разделе [Трассировка действий WMI](tracing-wmi-activity.md). Windows Поставщики модели драйвера (WDM) продолжают вести журнал в файле Вбемпров. log.

## <a name="wmi-log-files"></a>Файлы журналов WMI

Служба WMI и некоторые поставщики записывают текстовые файлы журнала для записи событий.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Файлы журналов поставщика WMI](wmi-provider-log-files.md)
</dt> <dd>

Поставщики WMI также могут поддерживать журналы. Файлы журналов, отображаемые в системе, зависят от того, какие поставщики установлены.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по инструментарию WMI](wmi-reference.md)
</dt> <dt>

[Трассировка действий WMI](tracing-wmi-activity.md)
</dt> <dt>

[Ведение журнала действий WMI](logging-wmi-activity.md)
</dt> </dl>

 

 
