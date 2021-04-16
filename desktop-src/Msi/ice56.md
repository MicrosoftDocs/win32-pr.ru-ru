---
description: ICE56 проверяет, что структура каталогов MSI-файла имеет единственный корневой каталог, что корень является свойством TARGETDIR, а значение свойства SourceDir — в столбце Дефаултдир таблицы Directory.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664035"
---
# <a name="ice56"></a>ICE56

ICE56 проверяет, что структура каталогов MSI-файла имеет единственный корневой каталог, что корень является свойством [**targetDir**](targetdir.md) , а значение свойства [**SourceDir**](sourcedir.md) — в столбце дефаултдир [таблицы Directory](directory-table.md).

Если MSI-файл имеет несколько корней или указывает корень, отличный от [**targetDir**](targetdir.md), [Административная установка](administrative-installation.md) не создает правильный административный образ.

Обратите внимание, что пустые каталоги не проверяются с помощью ICE56. Структура каталогов проходит проверку с несколькими корневыми каталогами, если лишние каталоги пусты.

## <a name="result"></a>Результат

ICE56 отправляет сообщение об ошибке, если MSI не имеет одного корня, [**targetDir**](targetdir.md)или если [**SourceDir**](sourcedir.md) не указан в столбце дефаултдир [таблицы Directory](directory-table.md).

## <a name="example"></a>Пример

ICE56 сообщает о следующих ошибках в приведенном примере.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Таблица каталога](directory-table.md)



| Каталог | \_Родительский каталог | дефаултдир |
|-----------|-------------------|------------|
| TARGETDIR |                   | Temp       |
| Root2     | Root2             | SourceDir  |



 

Чтобы исправить первую ошибку, корневой элемент [**targetDir**](targetdir.md) должен иметь значение дефаултдир, равное [**SourceDir**](sourcedir.md). SOURCEDIR также принимается. Можно сделать так, чтобы параметр **targetDir** был родителем второго корня и использовал значение "." в столбце дефаултдир. Дополнительные сведения см. в [таблице Directory](directory-table.md) .

Чтобы устранить вторую ошибку, структура каталогов должна иметь только один корень с именем [**targetDir**](targetdir.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



