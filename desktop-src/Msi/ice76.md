---
description: ICE76 проверяет использование каталога SFP (WFP) в пакетах установщик Windows для Windows Me. Этот ICE также проверяет отсутствие файлов в справочнике по таблицам BindImage.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650579"
---
# <a name="ice76"></a>ICE76

ICE76 проверяет использование каталога SFP (WFP) в пакетах установщик Windows для Windows Me. Этот ICE также проверяет отсутствие файлов в справочнике по [таблицам](bindimage-table.md) BindImage.

Для защиты файлов Windows требуется точное соответствие между файлом и подписью, внедренной в файл каталога. Файлы, ссылающиеся на каталог SFP, не должны быть перечислены в таблице BindImage, так как [действие BindImage](bindimage-action.md) для этих файлов различается на разных компьютерах. Файлы, на которые ссылаются каталоги SFP, должны находиться в компонентах, которые являются постоянными или установлены локально.

## <a name="result"></a>Результат

ICE76 отправляет ошибку для каждого файла в [таблице BindImage](bindimage-table.md) , которая также находится в [таблице филесфпкаталог](filesfpcatalog-table.md).

ICE76 выводит ошибку, если файл в таблице Филесфпкаталог принадлежит компоненту со следующим значением true:

-   **мсидбкомпонентаттрибутесперманент** не задан в столбце Attributes [таблицы Component](component-table.md).
-   **мсидбкомпонентаттрибутессаурцеонли** задается в столбце Attributes таблицы Component.
-   **мсидбаттрибутесоптионал** задается в столбце Attributes таблицы Component.

## <a name="example"></a>Пример

ICE76 сообщает о следующей ошибке в примере:

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[Таблица филесфпкаталог](filesfpcatalog-table.md) (частичная)



| Файл\_ | сфпкаталог\_ |
|--------|--------------|
| Файл1  | Catalog1.Cat |



 

[Таблица BindImage](bindimage-table.md) (частичная)



| Файл\_ |
|--------|
| Файл1  |



 

Чтобы исправить это, не вводите файлы, ссылающиеся на каталоги SFP, в таблицу BindImage.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Таблица BindImage](bindimage-table.md)
</dt> <dt>

[Таблица компонентов](component-table.md)
</dt> <dt>

[Таблица Филесфпкаталог](filesfpcatalog-table.md)
</dt> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



