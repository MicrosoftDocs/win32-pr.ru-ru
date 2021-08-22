---
title: Media.name
description: Свойство Name указывает или получает имя элемента мультимедиа.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abe6df00b5674cfbd443a5838b208814e30c5ecf75875586907314fc3a39d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616860"
---
# <a name="medianame"></a>Media.name

Свойство **Name** указывает или получает имя элемента мультимедиа.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *куррентмедиа*. **имя**

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи, содержащей имя элемента мультимедиа.

## <a name="remarks"></a>Remarks

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Чтобы указать значение этого свойства, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Перед использованием этого метода для указания имени элемента мультимедиа используйте **исреадонлитем** , чтобы определить, можно ли задать имя.

**проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *носитель*. **имя** для изменения имени текущего элемента мультимедиа. HTML-элемент ввода текста с именем Наметекст позволяет пользователю ввести текстовую строку для нового имени. Объект **Player** создан с идентификатором "Player".


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





