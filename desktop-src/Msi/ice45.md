---
description: ICE45 проверяет, что столбцы битовых полей в базе данных не задают Зарезервированные биты равными 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264182"
---
# <a name="ice45"></a>ICE45

ICE45 проверяет, что столбцы битовых полей в базе данных не задают Зарезервированные биты равными 1.

Зарезервированные биты не предоставляют функциональных возможностей в текущих версиях установщика, но могут в будущих версиях. Для них необходимо задать значение 0, чтобы они были совместимы с будущими версиями установщик Windows.

## <a name="result"></a>Результат

ICE45 отправляет сообщение об ошибке, если любая из следующих таблиц содержит битовое поле, для которого зарезервированный бит имеет значение 1.

-   [Таблица Ббконтрол](bbcontrol-table.md)
-   [Таблица диалоговых окон](dialog-table.md)
-   [Таблица функций](feature-table.md)
-   [Таблица файлов](file-table.md)
-   [Таблица MoveFile](movefile-table.md)
-   [Таблица Модулеконфигуратион](moduleconfiguration-table.md)
-   [Таблица Одбкдатасаурце](odbcdatasource-table.md)
-   [Таблица исправлений](patch-table.md)
-   [Таблица Ремовефиле](removefile-table.md)
-   [Таблица ServiceControl](servicecontrol-table.md)
-   [Таблица Сервицеинсталл](serviceinstall-table.md)
-   [Таблица система создала шрифт](textstyle-table.md)

ICE45 отправляет одно из двух предупреждений, если в [таблице элементов управления](control-table.md) содержится битовое поле с зарезервированным битом, равным значению 1.

## <a name="example"></a>Пример

ICE45 сообщает об ошибке в приведенном примере.

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

ICE45 сообщает следующее предупреждение для приведенного примера.

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

[Таблица файлов](file-table.md) (частичная)



| Файл  | Атрибуты |
|-------|------------|
| Файл1 | 128        |



 

[Таблица управления](control-table.md) (частичная)



| Диалог  | Control | Атрибуты |
|---------|---------|------------|
| Dialog1 | Edit1   | 2097152    |
| Dialog1 | Edit2   | 1048576    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



