---
title: сопоставление цветов проигрыватель Windows Media
description: сопоставление цветов проигрыватель Windows Media
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- проигрыватель Windows Media интернет-магазинов, сопоставление цветов проигрыватель Windows Media
- интернет-магазины, сопоставление цветов проигрыватель Windows Media
- тип 1 интернет-магазины, сопоставление цветов проигрыватель Windows Media
- тип 2 интернет-магазинов, сопоставление цветов проигрыватель Windows Media
- проигрыватель Windows Media интернет-магазинов, проигрыватель Windows Media сопоставление цветов
- интернет-магазины, проигрыватель Windows Media сопоставление цветов
- тип 1 интернет-магазины, проигрыватель Windows Media сопоставление цветов
- тип 2 интернет-магазинов, проигрыватель Windows Media сопоставление цветов
- проигрыватель Windows Media интернет-магазинов, сопоставление цветов для проигрыватель Windows Media
- интернет-магазины, сопоставление цветов для проигрыватель Windows Media
- тип 1 интернет-магазины, сопоставление цветов для проигрыватель Windows Media
- тип 2 интернет-магазинов, сопоставление цветов для проигрыватель Windows Media
- сопоставление цветов для проигрыватель Windows Media
- соответствие цветов проигрыватель Windows Media
- проигрыватель Windows Media, соответствующие цвета
- проигрыватель Windows Media, сопоставление цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3dbb7ed8b73973d35bc8ad884109c569d1c4738d038cf48f657068c5bde51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135187"
---
# <a name="matching-the-windows-media-player-colors"></a>сопоставление цветов проигрыватель Windows Media

чтобы веб-страница интернет-магазина соответствовала цветовой схеме проигрыватель Windows Media, достаточно просто. Просто обработайте событие **External. онколорчанже** . Чтобы указать функцию для работы с событием, используйте код, подобный приведенному ниже, при загрузке веб-страницы:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



каждый раз, когда пользователь изменяет цветовую схему проигрыватель Windows Media, игрок вызывает функцию. В следующем примере показана простая функция, которая задает фон веб-страницы в соответствии со свойством **External. аппколорлигхт** :


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



Существуют и другие свойства цвета, доступные для использования. См. [внешний объект для Интернет-магазинов типа 2](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**External. Аппколорлигхт**](external-appcolorlight.md)
</dt> <dt>

[**Внешнее событие Онколорчанже**](external-oncolorchange-event.md)
</dt> <dt>

[**Сведения, общие для типа 1 и 2 Интернет-магазинов**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




