---
description: В таблице с рекламным объявлением перечислены элементы управления объявлением, отображаемые в полном пользовательском интерфейсе.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Таблица объявлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998264"
---
# <a name="billboard-table"></a>Таблица объявлений

В таблице с рекламным объявлением перечислены [элементы управления объявлением](billboard-control.md) , отображаемые в полном пользовательском интерфейсе.

Таблица объявлений содержит следующие столбцы.



| Столбец    | Type                         | Ключ | Допускает значения NULL |
|-----------|------------------------------|-----|----------|
| Печат | [Идентификатор](identifier.md) | Да   | Нет        |
| Функция\_ | [Идентификатор](identifier.md) | Нет   | Нет        |
| Действие    | [Идентификатор](identifier.md) | Нет   | Да        |
| Упорядочение  | [Integer](integer.md)       | Нет   | Да        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Печат
</dt> <dd>

Имя [элемента управления объявлением](billboard-control.md).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_
</dt> <dd>

Внешний ключ к первому столбцу [таблицы Feature](feature-table.md). Объявление отображается только в том случае, если эта функция установлена.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки
</dt> <dd>

Имя действия. Объявление отображается во время выполнения сообщений, полученных от этого действия.

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Упорядочение
</dt> <dd>

При наличии нескольких объявлений, соответствующих действию, они отображаются в порядке, определенном в этом столбце. Это число не должно быть отрицательным.

</dd> </dl>

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



