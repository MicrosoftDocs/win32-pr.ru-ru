---
description: ICEM11 проверяет, что настраиваемый модуль слияния содержит таблицу Модулеконфигуратион и таблицу Модулесубститутион в таблице Модулеигноретабле модуля.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 157248d62f43a0b1a791220e2aeb917ba8273d31b93de69078f9876cddbd2748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894434"
---
# <a name="icem11"></a>ICEM11

ICEM11 проверяет, что настраиваемый модуль слияния содержит [таблицу модулеконфигуратион](moduleconfiguration-table.md) и [таблицу Модулесубститутион](modulesubstitution-table.md) в [таблице модулеигноретабле](moduleignoretable-table.md) модуля. Это гарантирует, что средства слияния, которые не распознают настраиваемые модули слияния (меньше версии 2,0), не копируют эти таблицы в целевую базу данных.

этот ицем доступен в файле мержемод. cub, который входит в состав пакета SDK для установщик Windows 2,0 и более поздних версий. дополнительные сведения см. в разделе [Windows SDK компонентов для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).

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
| Элемент | Dialog1; Control1 | Текст   | \[IconKey1\] |



 

[модулеигноретабле](moduleignoretable-table.md)



| Таблица               |
|---------------------|
| модулеконфигуратион |



 

Чтобы устранить эту ошибку, включите в таблицу Модулеигноретабле таблицы Модулесубститутион и Модулеконфигуратион.

## <a name="table-used-during-execution"></a>Таблица, используемая во время выполнения

[модулесубститутион](modulesubstitution-table.md)

[модулеконфигуратион](moduleconfiguration-table.md)

[модулеигноретабле](moduleignoretable-table.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



