---
description: Поставщик Вмиперфкласс и поставщик Вмиперфинст динамически предоставляют данные счетчиков производительности для классов счетчиков производительности WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Библиотеки производительности и инструментарий WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701787"
---
# <a name="performance-libraries-and-wmi"></a>Библиотеки производительности и инструментарий WMI

[Поставщик вмиперфкласс](wmiperfclass-provider.md) и [поставщик вмиперфинст](wmiperfinst-provider.md) динамически предоставляют данные счетчиков производительности для [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Поставщики Вмиперфкласс и Вмиперфинст

[Поставщик вмиперфкласс](wmiperfclass-provider.md) создает [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI при инициализации системы. [Поставщик вмиперфинст](wmiperfinst-provider.md) динамически предоставляет данные счетчиков производительности для этих классов. Поставщик поставщика Вмиперфкласс предоставляет классы для [счетчиков производительности](/windows/desktop/PerfCtrs/performance-counters-portal)версии 1 и версии 2.

Счетчики версии 1 находятся в реестре в разделе **hKey \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services**. Службы, предоставляющие данные о производительности, имеют подраздел **производительности** . Классы производительности WMI, созданные из счетчиков версии 1, не имеют "счетчиков" в составе имени.

**Идентификатор GUID**, определяющий поставщик счетчика производительности версии 2, находится в реестре в разделе **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ PerfLib \\ \_ V2Providers**.

Вмиперфкласс регистрируется как стандартный поставщик классов WMI. Вмиперфинст — это поставщик экземпляров WMI, предоставляющий данные из модуля поддержки данных производительности (PDH) для счетчиков версии 1 и версии 2. Дополнительные сведения см. в разделе [Использование функций PDH для использования данных счетчика](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения об инструментарии WMI](about-wmi.md)
</dt> <dt>

[Мониторинг данных производительности](monitoring-performance-data.md)
</dt> </dl>

 

 
