---
title: Считывание значений атрибутов
description: Считывание значений атрибутов
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Проигрыватель Windows Media, атрибуты для элементов мультимедиа
- Объектная модель проигрывателя Windows Media, атрибуты элементов мультимедиа
- Объектная модель, атрибуты элементов мультимедиа
- Проигрыватель Windows Media Mobile, атрибуты для элементов мультимедиа
- Элемент управления ActiveX проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Элемент управления ActiveX, атрибуты для элементов мультимедиа
- Библиотека проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Библиотека, атрибуты для элементов мультимедиа
- атрибуты, чтение значений
- считывание значений атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700661"
---
# <a name="reading-attribute-values"></a>Считывание значений атрибутов

Атрибуты, которые можно найти в библиотеке и в файлах Windows Media, имеют предопределенные имена. Можно написать код, извлекающий значение одного атрибута, передав имя этого атрибута на *носитель*. **getItemInfo** или *Media*. **жетитеминфобитипе**. Можно также написать код, извлекающий значения всех атрибутов в файле или элементе.

Следующий пример на C# извлекает значение атрибута **Title** и отображает его в окне сообщения. В этом примере объект **Player** был определен как проигрыватель Аксвмплиб. аксвиндовсмедиаплайер.


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



В вызове **жетитеминфобитипе** вторым параметром является строка, указывающая язык. Если передать пустую строку, как показано в этом примере, метод извлекает значение на языке по умолчанию. Дополнительные сведения о третьем параметре см. в разделе [атрибуты с несколькими значениями](attributes-with-multiple-values.md).

Следующий пример на C# извлекает значения для данного атрибута в текущем элементе мультимедиа. Он возвращает эти значения в виде строки, разделенной точкой с запятой. Обратите внимание, что для атрибутов, представленных в виде объектов, таких как **WM/песни \_ синхронизированы**, **WM/Picture**, и **WM/усервебурл**, функция возвращает пустую строку.


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



Третьим аргументом, передаваемым методу **жетитеминфобитипе** , является индекс определенного атрибута в наборе атрибутов с тем же именем.

Аналогичный код можно использовать для получения атрибутов с уникальными именами. В таких случаях **жетаттрибутекаунтбитипе** возвращает 1. В приведенном выше примере вызов **жетитеминфобитипе** будет выполняться только один раз.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Изменение значений атрибутов**](changing-attribute-values.md)
</dt> <dt>

[**Атрибуты элемента мультимедиа**](media-item-attributes.md)
</dt> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Считывание значений атрибутов с компакт-диска или DVD-диска**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




