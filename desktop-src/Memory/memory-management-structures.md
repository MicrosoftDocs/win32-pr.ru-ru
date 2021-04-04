---
description: 'Для управления памятью используются следующие структуры:'
ms.assetid: 02a2a874-9ced-4b7d-8aad-4a7768639a32
title: Структуры управления памятью
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: dc9f2837941c26f0ff9fed5b7d65a00f6bd254a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999682"
---
# <a name="memory-management-structures"></a>Структуры управления памятью

Для управления памятью используются следующие структуры.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**\_ \_ сведения о цели вызова cfg \_**](-cfg-call-target-info.md) | Представляет сведения о целевых объектах вызова для защиты потока управления (CFG). |
| [**\_ \_ сведения о оптимизации ресурсов кучи \_**](/windows/desktop/api/winnt/ns-winnt-heap_optimize_resources_information) | Задает флаги для операции Хеапоптимизересаурцес, инициированной с помощью [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation). |
| [**\_требования к адресу памяти \_**](/windows/desktop/api/winnt/ns-winnt-mem_address_requirements) | Задает наименьший и максимальный базовый адрес и выравнивание в составе расширенного параметра функции, управляющей виртуальной памятью. |
| [**MEM, \_ Расширенный \_ параметр**](/windows/desktop/api/winnt/ns-winnt-mem_extended_parameter) | Представляет расширенный параметр для функции, управляющей виртуальной памятью. |
| [**\_основные \_ сведения о памяти**](/windows/desktop/api/winnt/ns-winnt-memory_basic_information) | Содержит сведения о диапазоне страниц в виртуальном адресном пространстве процесса. |
| [**MEMORYSTATUS**](/windows/desktop/api/WinBase/ns-winbase-memorystatus) | Содержит сведения о текущем состоянии физической и виртуальной памяти. |
| [**мемористатусекс**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-memorystatusex) | Содержит сведения о текущем состоянии физической и виртуальной памяти, включая расширенную память. |
| [**\_запись КУЧИ \_ процесса**](/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry) | Содержит сведения об элементе heap. |
| [**\_ \_ Запись диапазона памяти \_ Win32**](/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_range_entry) | Указывает диапазон памяти. |
| [**\_ \_ Сведения о области памяти Win32 \_**](/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_region_information) | Содержит сведения о области памяти. |
| [**Атлсункдата \_ t**](/previous-versions/windows/desktop/legacy/mt805050(v=vs.85)) | Непрозрачная структура данных, представляющая собой преобразователь ATL. |
