---
title: Соответствующие цвета проигрывателя Windows Media
description: Соответствующие цвета проигрывателя Windows Media
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player — Интернет-магазины, соответствующие цвета проигрывателя Windows Media
- Интернет-магазины, соответствующие цвета проигрывателя Windows Media
- Тип 1 Интернет-магазины, соответствующие цвета проигрывателя Windows Media
- Тип 2 Интернет-магазинов, соответствующие цвета проигрывателя Windows Media
- Интернет-магазины проигрывателя Windows Media, сопоставление цветов проигрывателя Windows Media
- Интернет-магазины, сопоставление цветов проигрывателем Windows Media
- Тип 1 Интернет-магазины, сопоставление цветов проигрывателя Windows Media
- Тип 2 Интернет-магазинов, сопоставление цветов проигрывателя Windows Media
- Интернет-магазины проигрывателя Windows Media, сопоставление цветов для проигрывателя Windows Media
- Интернет-магазины, сопоставление цветов для проигрывателя Windows Media
- Тип 1 Интернет-магазины, сопоставление цветов для проигрывателя Windows Media
- Тип 2. Интернет-магазины, сопоставление цветов для проигрывателя Windows Media
- Сопоставление цветов для проигрывателя Windows Media
- соответствующие цвета проигрывателя Windows Media
- Проигрыватель Windows Media, сопоставление цветов
- Проигрыватель Windows Media, сопоставление цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700665"
---
# <a name="matching-the-windows-media-player-colors"></a>Соответствующие цвета проигрывателя Windows Media

Создание веб-страницы Интернет-магазина с помощью цветовой схемы проигрывателя Windows Media — это просто. Просто обработайте событие **External. онколорчанже** . Чтобы указать функцию для работы с событием, используйте код, подобный приведенному ниже, при загрузке веб-страницы:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Каждый раз, когда пользователь изменяет цветовую схему проигрывателя Windows Media, проигрыватель вызывает функцию. В следующем примере показана простая функция, которая задает фон веб-страницы в соответствии со свойством **External. аппколорлигхт** :


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



Существуют и другие свойства цвета, доступные для использования. См. [внешний объект для Интернет-магазинов типа 2](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**External. Аппколорлигхт**](external-appcolorlight.md)
</dt> <dt>

[**Внешнее событие Онколорчанже**](external-oncolorchange-event.md)
</dt> <dt>

[**Сведения, общие для типа 1 и 2 Интернет-магазинов**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




