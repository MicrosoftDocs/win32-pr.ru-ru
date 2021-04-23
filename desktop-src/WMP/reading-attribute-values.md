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
# <a name="reading-attribute-values"></a><span data-ttu-id="f6017-114">Считывание значений атрибутов</span><span class="sxs-lookup"><span data-stu-id="f6017-114">Reading Attribute Values</span></span>

<span data-ttu-id="f6017-115">Атрибуты, которые можно найти в библиотеке и в файлах Windows Media, имеют предопределенные имена.</span><span class="sxs-lookup"><span data-stu-id="f6017-115">The attributes you can find in the library and in Windows Media files have predefined names.</span></span> <span data-ttu-id="f6017-116">Можно написать код, извлекающий значение одного атрибута, передав имя этого атрибута на *носитель*. **getItemInfo** или *Media*. **жетитеминфобитипе**.</span><span class="sxs-lookup"><span data-stu-id="f6017-116">You can write code that retrieves the value of one attribute by passing the name of that attribute to *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="f6017-117">Можно также написать код, извлекающий значения всех атрибутов в файле или элементе.</span><span class="sxs-lookup"><span data-stu-id="f6017-117">You can also write code that retrieves the values of all of the attributes in a file or item.</span></span>

<span data-ttu-id="f6017-118">Следующий пример на C# извлекает значение атрибута **Title** и отображает его в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="f6017-118">The following C# example retrieves the value of the **Title** attribute and displays it in a message box.</span></span> <span data-ttu-id="f6017-119">В этом примере объект **Player** был определен как проигрыватель Аксвмплиб. аксвиндовсмедиаплайер.</span><span class="sxs-lookup"><span data-stu-id="f6017-119">In this example, the **Player** object was defined as axWMPLib.AxWindowsMediaPlayer Player.</span></span>


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



<span data-ttu-id="f6017-120">В вызове **жетитеминфобитипе** вторым параметром является строка, указывающая язык.</span><span class="sxs-lookup"><span data-stu-id="f6017-120">In the call to **getItemInfoByType**, the second parameter is a string that specifies the language.</span></span> <span data-ttu-id="f6017-121">Если передать пустую строку, как показано в этом примере, метод извлекает значение на языке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f6017-121">If you pass an empty string as shown in this example, the method retrieves the value in the default language.</span></span> <span data-ttu-id="f6017-122">Дополнительные сведения о третьем параметре см. в разделе [атрибуты с несколькими значениями](attributes-with-multiple-values.md).</span><span class="sxs-lookup"><span data-stu-id="f6017-122">For information about the third parameter, see [Attributes with Multiple Values](attributes-with-multiple-values.md).</span></span>

<span data-ttu-id="f6017-123">Следующий пример на C# извлекает значения для данного атрибута в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f6017-123">The following C# example retrieves the values for a given attribute in the current media item.</span></span> <span data-ttu-id="f6017-124">Он возвращает эти значения в виде строки, разделенной точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="f6017-124">It returns these values as a semicolon-delimited string.</span></span> <span data-ttu-id="f6017-125">Обратите внимание, что для атрибутов, представленных в виде объектов, таких как **WM/песни \_ синхронизированы**, **WM/Picture**, и **WM/усервебурл**, функция возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="f6017-125">Note that for attributes represented as objects, such as **WM/Lyrics\_Synchronised**, **WM/Picture**, and **WM/UserWebURL**, the function returns an empty string.</span></span>


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



<span data-ttu-id="f6017-126">Третьим аргументом, передаваемым методу **жетитеминфобитипе** , является индекс определенного атрибута в наборе атрибутов с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="f6017-126">The third argument passed to the **getItemInfoByType** method is the index of a particular attribute in a set of attributes with the same name.</span></span>

<span data-ttu-id="f6017-127">Аналогичный код можно использовать для получения атрибутов с уникальными именами.</span><span class="sxs-lookup"><span data-stu-id="f6017-127">You can use similar code to retrieve attributes that have unique names.</span></span> <span data-ttu-id="f6017-128">В таких случаях **жетаттрибутекаунтбитипе** возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="f6017-128">In those cases, **getAttributeCountByType** returns 1.</span></span> <span data-ttu-id="f6017-129">В приведенном выше примере вызов **жетитеминфобитипе** будет выполняться только один раз.</span><span class="sxs-lookup"><span data-stu-id="f6017-129">In the example shown earlier, the call to **getItemInfoByType** would execute only once.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6017-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f6017-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6017-131">**Изменение значений атрибутов**</span><span class="sxs-lookup"><span data-stu-id="f6017-131">**Changing Attribute Values**</span></span>](changing-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="f6017-132">**Атрибуты элемента мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="f6017-132">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6017-133">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="f6017-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f6017-134">**Считывание значений атрибутов с компакт-диска или DVD-диска**</span><span class="sxs-lookup"><span data-stu-id="f6017-134">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




