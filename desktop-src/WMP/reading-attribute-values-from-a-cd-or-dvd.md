---
title: Считывание значений атрибутов с компакт-диска или DVD-диска
description: Считывание значений атрибутов с компакт-диска или DVD-диска
ms.assetid: 441916fb-f66d-4a12-a95c-b47561c93e64
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
ms.openlocfilehash: 8909a752e9a974e4959be8ecd933d4bb3f1bfd4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331627"
---
# <a name="reading-attribute-values-from-a-cd-or-dvd"></a><span data-ttu-id="36f96-114">Считывание значений атрибутов с компакт-диска или DVD-диска</span><span class="sxs-lookup"><span data-stu-id="36f96-114">Reading Attribute Values from a CD or DVD</span></span>

<span data-ttu-id="36f96-115">В этом разделе объект **Player** был определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="36f96-115">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="36f96-116">В следующем примере кода на языке C# извлекаются значения всех атрибутов в текущем диске, которые находятся на диске, и записываются в файл.</span><span class="sxs-lookup"><span data-stu-id="36f96-116">The following C# example code retrieves the values of all attributes in the current disc that is in the drive and writes them to a file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="36f96-117">См. также</span><span class="sxs-lookup"><span data-stu-id="36f96-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36f96-118">**Атрибуты элемента мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="36f96-118">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="36f96-119">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="36f96-119">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 




