---
description: ICE66 использует таблицы в базе данных для определения схемы, которую должна использовать база данных.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810912"
---
# <a name="ice66"></a>ICE66

ICE66 использует таблицы в базе данных для определения схемы, которую должна использовать база данных.

Некоторые функциональные возможности могут быть доступны только в том случае, если пакет установлен в системе с текущей версией установщик Windows.

## <a name="result"></a>Результат

ICE66 отправляет предупреждение, если в базе данных используется неправильная схема.

## <a name="example"></a>Пример

ICE66 сообщает следующее предупреждение для приведенного примера.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

Это предупреждение можно пропустить, если вы хотите, чтобы пакет был установлен с использованием текущей версии установщик Windows. Например, если вы хотите, чтобы пакет был установлен только в версии 2,0 или более поздней, измените схему пакета (PID \_ PAGECOUNT) на 200.

[Таблица Исолатедкомпонент](isolatedcomponent-table.md)



| \_Общий компонент | \_Приложение компонента |
|-------------------|------------------------|
| Component1        | Component2             |



 

[Сводный поток информации](summary-information-stream.md)



| пидт           | Значение |
|----------------|-------|
| Идентификатор процесса \_ PAGECOUNT | 100   |



 

## <a name="table-used-during-execution"></a>Таблица, используемая во время выполнения:

[\_Таблица Columns](-columns-table.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



