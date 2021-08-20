---
description: ICE66 использует таблицы в базе данных для определения схемы, которую должна использовать база данных.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023450a451a412c47c21904ab96a13e4513c71f8327966dffa5b657b1b65bb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787404"
---
# <a name="ice66"></a>ICE66

ICE66 использует таблицы в базе данных для определения схемы, которую должна использовать база данных.

некоторые функциональные возможности могут быть доступны только в том случае, если пакет установлен в системе с текущей версией установщик Windows.

## <a name="result"></a>Результат

ICE66 отправляет предупреждение, если в базе данных используется неправильная схема.

## <a name="example"></a>Пример

ICE66 сообщает следующее предупреждение для приведенного примера.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

это предупреждение можно пропустить, если вы хотите, чтобы пакет был установлен с использованием текущей версии установщик Windows. Например, если вы хотите, чтобы пакет был установлен только в версии 2,0 или более поздней, измените схему пакета (PID \_ PAGECOUNT) на 200.

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



