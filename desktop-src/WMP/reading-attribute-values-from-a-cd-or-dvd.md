---
title: Считывание значений атрибутов с компакт-диска или DVD-диска
description: Считывание значений атрибутов с компакт-диска или DVD-диска
ms.assetid: 441916fb-f66d-4a12-a95c-b47561c93e64
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
ms.openlocfilehash: 800fda1bf3002f015873b69e29503ecba637a978bac1b167724c04f5f15228b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861774"
---
# <a name="reading-attribute-values-from-a-cd-or-dvd"></a>Считывание значений атрибутов с компакт-диска или DVD-диска

В этом разделе объект **Player** был определен следующим образом:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



В следующем примере кода на языке C# извлекаются значения всех атрибутов в текущем диске, которые находятся на диске, и записываются в файл.


```C++
private void logDiscAttributes()
{
    int iCDCount = 0; // Count of CD and DVD drives
    int iAttrCount = 0; // Attribute count.
    int iPLCount = 0; // Playlist item count.

    IWMPCdromCollection cdCollection;
    IWMPPlaylist playlist;
    IWMPMedia media;
    string strAttribName = "";
    string strAttribValue = "";
    string strText = "";

    // Create a StreamWriter object to write
    // the output to a file.
    StreamWriter sw = new StreamWriter(strOutFile, true);

    cdCollection = Player.cdromCollection;
    iCDCount = cdCollection.count;

    // Loop through the CD and DVD drives.
    for (int i = 0; i < iCDCount; i++)
    {
        playlist = cdCollection.Item(i).Playlist;

        // Loop through the playlist attributes.
        iAttrCount = playlist.attributeCount;
        for (int j = 0; j < iAttrCount; j++)
        {
            strText += "Playlist Attribute: \t";
            strAttribName = playlist.get_attributeName(j);
            strText += "\t" + strAttribName + "\t";
            strAttribValue = playlist.getItemInfo(strAttribName);
            strText += strAttribValue + "\n";
        }

        // Loop through the playlist.
        iPLCount = playlist.count;
        for (int k = 0; k < iPLCount; k++)
        {
            media = playlist.get_Item(k);

            // Loop through the media attributes.
            iAttrCount = media.attributeCount;
            for (int m = 0; m < iAttrCount; m++)
            {
                strText += "Track or Chapter [" + m.ToString() + "]";
                strAttribName = media.getAttributeName(m);
                strText += "\t" + strAttribName + "\t";
                strText += "Read Only: " + media.isReadOnlyItem(strAttribName) + "\t";
                strAttribValue = media.getItemInfo(strAttribName);
                strText += strAttribValue + "\n";
            }
        }
    }

    sw.Write(strText);
    sw.Close();

    MessageBox.Show(strOutFile + " created");
}

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Атрибуты элемента мультимедиа**](media-item-attributes.md)
</dt> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> </dl>

 

 




