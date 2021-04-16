---
title: Элемент TITLE (метафайл)
description: Элемент TITLE определяет текстовую строку, указывающую заголовок для элемента ASX или ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Элемент TITLE (метафайл) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708434"
---
# <a name="title-element-metafile"></a>Элемент TITLE (метафайл)

Элемент **Title** определяет текстовую строку, указывающую заголовок для элемента **ASX** или **entry** .

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элементы           |
|-----------------|--------------------|
| Родительские элементы | **ASX**, **запись** |
| Дочерние элементы  | Нет               |



 

## <a name="remarks"></a>Remarks

Этот элемент определяет текстовую строку, указывающую заголовок элемента **ASX** или **entry** . Заголовок отображается на панели отображения и в диалоговом окне **Свойства** .

Когда этот элемент появляется внутри элемента **ASX** , он отображается как **Показать** информацию. Когда этот элемент появляется в элементе **entry** , он отображается как сведения об **обрезке** .

Если элемент **мореинфо** также используется со связанным (родительским) элементом, это текст заголовка, который пользователь щелкает для доступа к URL-адресу, определенному в элементе **мореинфо** .

Каждый родительский элемент **ASX** и **entry** должен содержать не более одного дочернего элемента **Title** . Несколько элементов **Title** после первого будут пропущены и не будут отображаться.

## <a name="examples"></a>Примеры


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 70 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Справочник по элементам метафайлов Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Справочник по метафайлу Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





