---
description: Начиная с Windows Vista, этот поставщик создает классы счетчиков производительности WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Поставщик Вмиперфкласс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080890"
---
# <a name="wmiperfclass-provider"></a>Поставщик Вмиперфкласс

Начиная с Windows Vista, этот поставщик создает [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI. Данные динамически передаются этим классам производительности WMI поставщиком [вмиперфинст](wmiperfinst-provider.md) . Процесс автоопределения и автоочистки (ADAP) больше не передает объекты счетчиков производительности в классы производительности WMI в репозитории WMI. Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md).

Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md).

Хотя не рекомендуется разрабатывать новые объекты производительности, создавая высокопроизводительный поставщик WMI и зависящий от процесса [*обратных адаптеров ADAP*](gloss-r.md) для перемещения данных в библиотеки производительности, исключением является разработка WDM драйвера, предоставляющего данные о производительности. Несмотря на то, что процесс обратного адаптера продолжит работать в целях обратной совместимости, рекомендуется использовать [счетчики производительности версии 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Имя экземпляра [**\_ \_ Win32Provider**](--win32provider.md) этого поставщика — "вмиперфкласс".

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поставщики WMI](wmi-providers.md)
</dt> <dt>

[Библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Мониторинг данных производительности](monitoring-performance-data.md)
</dt> </dl>

 

 
