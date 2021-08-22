---
title: Элемент SKIN (не рекомендуется)
description: эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрыватель Windows Media и пакета SDK для проигрыватель Windows Media.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- элемент SKIN (не рекомендуется) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b868b756ed190301c66987b6e26249762bac71842f4a5425d6d7c6d4b16816a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507914"
---
# <a name="skin-element-deprecated"></a>Элемент SKIN (не рекомендуется)

эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрыватель Windows Media и пакета SDK для проигрыватель Windows Media.

Элемент **Skin** задает URL-адрес границы.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Атрибуты

**Href** (обязательно)

URL-адрес для файла сжатой границы с расширением WMZ. для проигрыватель Windows Media 9 Series или более поздней версии это значение может ссылаться только на файлы границ на жестком диске пользователя, расположенные в том же каталоге, что и список воспроизведения метафайлов. См. пример кода.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элементы |
|-----------------|----------|
| Родительские элементы | **ASX**  |
| Дочерние элементы  | Нет     |



 

## <a name="remarks"></a>Remarks

элемент **SKIN** используется для создания границы, которая аналогична обложке, но отображается в области **воспроизведение** в полноэкранном режиме проигрыватель Windows Media. элемент **SKIN** используется только для границ, которые отображаются в полноэкранном режиме проигрыватель Windows Media, а не для обычных обложек, которые полностью заменяют проигрыватель Windows Media в компактном режиме.

в пакете загрузки Windowsного носителя (с расширением имени файла. wmd) элемент **SKIN** позволяет границе иметь содержимое и ссылаться на другие сайты. пакет загрузки Windowsного носителя — это сжатый файл, содержащий файл границ и метафайл Windowsного мультимедиа. Файл границ (с расширением WMZ) сжимается и включает файл определения обложки (с расширением WMS).

Элемент **Skin** имеет три компонента:

-   Обложка
-   Некоторое содержимое
-   Метафайл

обложки, включаемые в пакеты загрузки мультимедиа Windows, должны быть прямоугольными в фигуре. Создание границ с непрямоугольными обложекми может привести к непредвиденным результатам.

## <a name="examples"></a>Примеры


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 70 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**границы для проигрыватель Windows Media (не рекомендуется)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Справочник по элементам метафайлов мультимедиа**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Ссылка на метафайл мультимедиа**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





