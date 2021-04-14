---
title: Добавление BUTTONGROUP
description: Добавление BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- Создание обложек, элемент BUTTONGROUP
- Обложки проигрывателя Windows Media, элемент BUTTONGROUP
- обложки, элемент BUTTONGROUP
- файлы определения обложки, элемент BUTTONGROUP
- BUTTONGROUP, элемент
- элементы, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329080"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание файла определения обложки**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




