---
description: ICE76 проверяет использование каталога SFP (WFP) в пакетах установщик Windows для Windows. Этот ICE также проверяет отсутствие файлов в справочнике по таблицам BindImage.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0b6caf5e29d26ba68721daa156dd0fc78a1868b5aa1ba1b7ea165834dd5ac8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129434"
---
# <a name="ice76"></a>ICE76

ICE76 проверяет использование каталога SFP (WFP) в пакетах установщик Windows для Windows. Этот ICE также проверяет отсутствие файлов в справочнике по [таблицам](bindimage-table.md) BindImage.

Windows Для защиты файлов требуется точное соответствие между файлом и подписью, внедренной в файл каталога. Файлы, ссылающиеся на каталог SFP, не должны быть перечислены в таблице BindImage, так как [действие BindImage](bindimage-action.md) для этих файлов различается на разных компьютерах. Файлы, на которые ссылаются каталоги SFP, должны находиться в компонентах, которые являются постоянными или установлены локально.

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



| File\_ | сфпкаталог\_ |
|--------|--------------|
| Файл1  | Catalog1.Cat |



 

[Таблица BindImage](bindimage-table.md) (частичная)



| File\_ |
|--------|
| Файл1  |



 

Чтобы исправить это, не вводите файлы, ссылающиеся на каталоги SFP, в таблицу BindImage.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Таблица BindImage](bindimage-table.md)
</dt> <dt>

[Таблица компонентов](component-table.md)
</dt> <dt>

[Таблица Филесфпкаталог](filesfpcatalog-table.md)
</dt> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



