---
title: Добавление BUTTONGROUP
description: Добавление BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- Создание обложек, элемент BUTTONGROUP
- обложки проигрыватель Windows Media, элемент BUTTONGROUP
- обложки, элемент BUTTONGROUP
- файлы определения обложки, элемент BUTTONGROUP
- BUTTONGROUP, элемент
- элементы, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6719bb3974b254f8d9446d45fd6d34385dbfcada4084c7bdd5c3a4e03bb06dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865193"
---
# <a name="adding-buttongroup"></a>Добавление BUTTONGROUP

В этом примере используется элемент **BUTTONGROUP** для написания кода в файле определения обложки. **BUTTONGROUP** создает простой способ обработки событий мыши без необходимости вычисления точных расположений на экране и использует цвет вместо координат x и y.

Сначала необходимо добавить теги **BUTTONGROUP** в созданный файл определения обложки. Вставьте их после атрибутов тега **темы** .


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Оставьте несколько пустых строк над закрывающим тегом **BUTTONGROUP** для кнопок, которые будут добавлены далее.

Для определения **BUTTONGROUP** используются следующие атрибуты:

**маппингимаже**

Это имя файла сопоставленного рисунка, созданного ранее, с красной и зеленой окружностями. Этот атрибут является обязательным для любого **BUTTONGROUP**.

**ховеримаже**

Это имя файла рисунка, который вы создали ранее, с двумя желтыми кнопками, которые считывают "Play" и "Close". Это не является обязательным, но изображение для наведения помогает отправить отзыв пользователю.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Создание файла определения обложки**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




