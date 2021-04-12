---
description: ICEM11 проверяет, что настраиваемый модуль слияния содержит таблицу Модулеконфигуратион и таблицу Модулесубститутион в таблице Модулеигноретабле модуля.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265419"
---
# <a name="icem11"></a>ICEM11

ICEM11 проверяет, что настраиваемый модуль слияния содержит [таблицу модулеконфигуратион](moduleconfiguration-table.md) и [таблицу Модулесубститутион](modulesubstitution-table.md) в [таблице модулеигноретабле](moduleignoretable-table.md) модуля. Это гарантирует, что средства слияния, которые не распознают настраиваемые модули слияния (меньше версии 2,0), не копируют эти таблицы в целевую базу данных.

Этот ИЦЕМ доступен в файле Мержемод. CUB, который входит в состав пакета SDK для установщик Windows 2,0 и более поздних версий. Дополнительные сведения см. в разделе [Windows SDK компонентов для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Результат

ICEM11 отправляет ошибку, если модуль содержит таблицу Модулеконфигуратион или Модулесубститутион, не указанную в таблице Модулеигноретабле.

## <a name="example"></a>Пример

ICEM11 отправляет следующие сообщения об ошибках для модуля, содержащего записи базы данных, показанные ниже.

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

[Модулеконфигуратион](moduleconfiguration-table.md) (частичный)



| Имя     | Формат | Тип   | контекстдата | DefaultValue |
|----------|--------|--------|-------------|--------------|
| IconKey1 | 1      | Двоичные данные | Значок        | дефаултикон  |



 

[модулесубститутион](modulesubstitution-table.md)



| Таблица   | Строка              | Столбец | Значение        |
|---------|------------------|--------|--------------|
| Control | Dialog1; Control1 | Текст   | \[IconKey1\] |



 

[модулеигноретабле](moduleignoretable-table.md)



| Таблица               |
|---------------------|
| модулеконфигуратион |



 

Чтобы устранить эту ошибку, включите в таблицу Модулеигноретабле таблицы Модулесубститутион и Модулеконфигуратион.

## <a name="table-used-during-execution"></a>Таблица, используемая во время выполнения

[модулесубститутион](modulesubstitution-table.md)

[модулеконфигуратион](moduleconfiguration-table.md)

[модулеигноретабле](moduleignoretable-table.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



