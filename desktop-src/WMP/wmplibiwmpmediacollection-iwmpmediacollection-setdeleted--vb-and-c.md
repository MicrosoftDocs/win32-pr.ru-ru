---
title: Ивмпмедиаколлектион Сетделетед, метод
description: Метод Сетделетед перемещает указанный элемент мультимедиа в папку Удаленные элементы. | Ивмпмедиаколлектион Сетделетед, метод
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- проигрыватель Windows Media метода сетделетед
- проигрыватель Windows Media метода сетделетед, интерфейс ивмпмедиаколлектион
- проигрыватель Windows Media интерфейса ивмпмедиаколлектион, метод сетделетед
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516d6aab26659fa2bba57bd961671b4dca0f92d367d5d9bb1f048e8fd19eb2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505954"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a>Метод Ивмпмедиаколлектион:: Сетделетед

`setDeleted`Метод перемещает указанный элемент мультимедиа в папку Удаленные элементы.

## <a name="syntax"></a>Синтаксис


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*питем* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмпмедиа** для перемещаемого элемента.

</dd> <dt>

*варфисделетед* \[ окне\]
</dt> <dd>

Значение **System. Boolean** , указывающее, следует ли перемещать элемент в папку "удаленные элементы". Это значение всегда должно быть **true**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод не удаляет файлы с компьютера пользователя, а просто перемещает их в папку Удаленные элементы.

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере используется `setDeleted` для перемещения определенного элемента мультимедиа в папку Удаленные элементы. Метод **IsDeleted** сначала проверяет, был ли уже удален элемент. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





