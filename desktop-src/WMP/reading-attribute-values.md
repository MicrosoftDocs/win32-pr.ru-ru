---
title: Считывание значений атрибутов
description: Считывание значений атрибутов
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- проигрыватель Windows Media, атрибуты для элементов мультимедиа
- объектная модель проигрыватель Windows Media, атрибуты для элементов мультимедиа
- Объектная модель, атрибуты элементов мультимедиа
- проигрыватель Windows Media Мобильные устройства, атрибуты элементов мультимедиа
- проигрыватель Windows Media ActiveX элемент управления, атрибуты для элементов мультимедиа
- проигрыватель Windows Media мобильный ActiveX элемент управления, атрибуты для элементов мультимедиа
- ActiveX элемент управления, атрибуты для элементов мультимедиа
- библиотека проигрыватель Windows Media, атрибуты для элементов мультимедиа
- Библиотека, атрибуты для элементов мультимедиа
- атрибуты, чтение значений
- считывание значений атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8431405b68435f41cb357a810e30c37bb96c5971824b3878b1982986aa0d0833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002834"
---
# <a name="reading-attribute-values"></a>Считывание значений атрибутов

атрибуты, которые можно найти в библиотеке и в Windows файлах мультимедиа, имеют предопределенные имена. Можно написать код, извлекающий значение одного атрибута, передав имя этого атрибута на *носитель*. **getItemInfo** или *Media*. **жетитеминфобитипе**. Можно также написать код, извлекающий значения всех атрибутов в файле или элементе.

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Изменение значений атрибутов**](changing-attribute-values.md)
</dt> <dt>

[**Атрибуты элемента мультимедиа**](media-item-attributes.md)
</dt> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Считывание значений атрибутов с компакт-диска или DVD-диска**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




