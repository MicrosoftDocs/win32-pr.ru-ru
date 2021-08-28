---
title: Ивмпмедиа. одинаковы (VB и C)
description: Свойство «идентично» (метод Get \_ одинаковы в C \) возвращает значение, указывающее, совпадает ли указанный элемент мультимедиа с текущим.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- ивмпмедиа. одинаковы (VB и C) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e8de133003bdddcf0438e5a13dc3fa74227ede7bf42350e2b7c3c96f2c197e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003584"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>Ивмпмедиа. одинаковы (VB и C#)

Свойство « **идентично** » (метод **Get \_ одинаковы** в C#) возвращает значение, указывающее, совпадает ли указанный элемент мультимедиа с текущим.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a>Параметры

*пивмпмедиа*

Интерфейс **вмплиб. ивмпмедиа** для элемента мультимедиа, сравниваемый с текущим элементом мультимедиа.

## <a name="property-value"></a>Значение свойства

Значение **System. Boolean** , указывающее, идентичны ли два элемента мультимедиа.

## <a name="remarks"></a>Remarks

**ивмпмедиа. идентично** — это свойство в Visual Basic, которое принимает параметр. В C# он называется **ивмпмедиа. Get \_ тождественным** методом.

## <a name="examples"></a>Примеры

В следующем примере используется свойство « **идентично** » (метод **Get \_ одинаковы** в C#), чтобы проверить, совпадает ли элемент мультимедиа с именем невмедиа и текущий элемент мультимедиа. Если они не совпадают, будет воспроизведен новый элемент мультимедиа. В противном случае текущий носитель продолжит воспроизводиться без прерывания. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

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
</dt> </dl>

 

 





