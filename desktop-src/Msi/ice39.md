---
description: ICE39 проверяет информационный поток сводки базы данных.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb912afbe7220eee1aa3bbcd494f6531736279b85c5736f6867fdf8779e39bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528444"
---
# <a name="ice39"></a>ICE39

ICE39 проверяет [информационный поток сводки](summary-information-stream.md) базы данных.

ICE39 проверяет формат следующих свойств:

-   [**Сводка по количеству слов**](word-count-summary.md)
-   [**Сводка по количеству страниц**](page-count-summary.md)
-   [**Сводка по шаблону**](template-summary.md)
-   [**Сводка по номеру редакции**](revision-number-summary.md)
-   [**Создать сводку по времени и дате**](create-time-date-summary.md)
-   [**Сводка по дате и времени последнего сохранения**](last-saved-time-date-summary.md)
-   [**Последняя выводимая сводка**](last-printed-summary.md)

Если в свойстве " [**Сводка слов**](word-count-summary.md) " указано, что источник сжат, ICE39 отправляет предупреждение, если какие-либо файлы также помечены как сжатые в столбце Attributes [таблицы File](file-table.md). См. раздел [Использование ящиков и сжатых источников](using-cabinets-and-compressed-sources.md).

ICE39 отправляет предупреждение, если в свойстве " [**Сводка слов**](word-count-summary.md) " указано, что пакет является совместимым с UAC, а [Таблица мсипаккажецертификате](msipackagecertificate-table.md) не пуста.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



