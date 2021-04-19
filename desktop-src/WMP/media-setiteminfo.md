---
title: Метод Media. Сетитеминфо
description: Метод Сетитеминфо задает значение указанного атрибута для текущего элемента мультимедиа.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Сетитеминфо метод Windows Media Player
- Сетитеминфо метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Сетитеминфо
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698817"
---
# <a name="mediasetiteminfo-method"></a>Метод Media. Сетитеминфо

Метод **сетитеминфо** задает значение указанного атрибута для текущего элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибут* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута. Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

</dd> <dt>

*значение* \[ окне\]
</dt> <dd>

**Строка** , содержащая новое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Свойство **аттрибутекаунт** содержит количество атрибутов, доступных для данного объекта **мультимедиа** . Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имен встроенных атрибутов, которые могут использоваться с этим методом.

Перед использованием этого метода используйте метод **исреадонлитем** , чтобы определить, можно ли задать определенный атрибут.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**Примечание**

При внедрении элемента управления проигрывателя Windows Media в приложение измененные атрибуты файла не будут записываться в файл мультимедиа до тех пор, пока пользователь не запустит проигрыватель Windows Media. При использовании элемента управления в удаленном приложении, написанном на языке C++, измененные атрибуты файла будут записаны в файл мультимедиа вскоре после внесения изменений. В любом случае изменения сразу же становятся доступными для кода через библиотеку.

**Проигрыватель Windows Media 10 Mobile:** Этот метод не реализован.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *носитель*. **сетитеминфо** , чтобы изменить значение атрибута жанра для текущего элемента мультимедиа. HTML-элемент ввода текста с именем genText позволяет пользователю ввести текстовую строку, которая затем будет использоваться для изменения сведений об атрибуте. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. Исреадонлитем**](media-isreadonlyitem.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





