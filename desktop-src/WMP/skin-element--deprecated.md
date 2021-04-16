---
title: Элемент SKIN (не рекомендуется)
description: Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Элемент SKIN (не рекомендуется) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657607"
---
# <a name="skin-element-deprecated"></a>Элемент SKIN (не рекомендуется)

Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.

Элемент **Skin** задает URL-адрес границы.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Атрибуты

**Href** (обязательно)

URL-адрес для файла сжатой границы с расширением WMZ. Для проигрывателя Windows Media 9 Series или более поздней версии это значение может ссылаться только на файлы границ на жестком диске пользователя, расположенные в том же каталоге, что и список воспроизведения метафайлов. См. пример кода.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элементы |
|-----------------|----------|
| Родительские элементы | **ASX**  |
| Дочерние элементы  | Нет     |



 

## <a name="remarks"></a>Remarks

Элемент **Skin** используется для создания границы, которая аналогична обложке, но отображается в области **Воспроизведение** в проигрывателе Windows Media в полноэкранном режиме. Элемент **Skin** используется только для границ, которые отображаются в проигрывателе Windows Media в полноэкранном режиме, а не для обычных обложек, которые полностью заменяют проигрыватель Windows Media в компактном режиме.

В пакете загрузки Windows Media (с расширением имени файла. WMD) элемент **Skin** позволяет границе иметь содержимое и ссылаться на другие сайты. Пакет загрузки Windows Media представляет собой сжатый файл, содержащий файл границ и метафайл Windows Media. Файл границ (с расширением WMZ) сжимается и включает файл определения обложки (с расширением WMS).

Элемент **Skin** имеет три компонента:

-   Обложка
-   Некоторое содержимое
-   Метафайл

Обложки, входящие в состав пакетов загрузки Windows Media, должны быть прямоугольными в фигуре. Создание границ с непрямоугольными обложекми может привести к непредвиденным результатам.

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 70 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Границы для проигрывателя Windows Media (не рекомендуется)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Справочник по элементам метафайлов Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Справочник по метафайлу Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





