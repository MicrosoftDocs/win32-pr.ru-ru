---
description: Таблица Extension содержит сведения о серверах расширений имен файлов, которые должны быть созданы как часть объявления продукта. Каждая строка создает набор разделов и значений реестра.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Таблица расширения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d664df812b723d7ab6c9b966b09fac8c57a35b655e123f720fdb87bdf431146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821744"
---
# <a name="extension-table"></a>Таблица расширения

Таблица Extension содержит сведения о серверах расширений имен файлов, которые должны быть созданы как часть объявления продукта. Каждая строка создает набор разделов и значений реестра.

Таблица Extension содержит столбцы, показанные в следующей таблице.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| Расширение   | [Text](text.md)             | Д   | Нет        |
| Компонент\_ | [Идентификатор](identifier.md) | Д   | Нет        |
| ID\_    | [Text](text.md)             | Нет   | Д        |
| ФОРМАТА\_      | [Text](text.md)             | Нет   | Д        |
| Компонент\_   | [Идентификатор](identifier.md) | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Продлен
</dt> <dd>

Расширение, связанное со строкой таблицы. Длина расширения может доставлять до 255 символов. Введите расширение в это поле без предшествующей точки.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ к первому столбцу таблицы [Component](component-table.md) . Этот столбец ссылается на компонент, управляющий установкой расширения.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ID\_
</dt> <dd>

Идентификатор программы, связанный с этим расширением. Это внешний ключ в таблице [ProgID](progid-table.md) .

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>ФОРМАТА\_
</dt> <dd>

Тип содержимого, который должен быть записан для столбца расширения.

Внешний ключ к первому столбцу таблицы [MIME](mime-table.md) .

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_
</dt> <dd>

Внешний ключ в первом столбце таблицы [Feature](feature-table.md) , указывающий компонент, предоставляющий сервер расширения.

</dd> </dl>

## <a name="remarks"></a>Remarks

Обращение к таблице расширений происходит при выполнении действия [регистерекстенсионинфо](registerextensioninfo-action.md) или [унрегистерекстенсионинфо](unregisterextensioninfo-action.md) .

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE69](ice69.md)  
</dl>

 

 



