---
title: Ивмпконтролс Плайитем, метод
description: Метод Плайитем воспроизводит указанный элемент мультимедиа. | Ивмпконтролс Плайитем, метод
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- проигрыватель Windows Media метода плайитем
- проигрыватель Windows Media метода плайитем, интерфейс ивмпконтролс
- проигрыватель Windows Media интерфейса ивмпконтролс, метод плайитем
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fabab78fe60120110f72176885e3b5825699b83782272dfbef0b48c165d1d02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761034"
---
# <a name="iwmpcontrolsplayitem-method"></a>Ивмпконтролс: метод:p Лайитем

Метод **плайитем** воспроизводит указанный элемент мультимедиа.

## <a name="syntax"></a>Синтаксис


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*пивмпмедиа* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмпмедиа** для элемента мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Элемент мультимедиа будет загружаться и воспроизводиться автоматически независимо от значения свойства **ивмпсеттингс. Автозапуск** . Чтобы загрузить элемент без автоматического воспроизведения, задайте для **ивмпсеттингс. автозапуска** значение **false** и присвойте значение **аксвиндовсмедиаплайер. URL**, после чего можно вызвать **ивмпконтролс. Play** , чтобы начать воспроизведение элемента.

Примечание

**плайитем** работает только с элементами в **аксвиндовсмедиаплайер. куррентплайлист**. Вызов **плайитем** со ссылкой на сохраненный элемент мультимедиа не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере **плайитем** используется для воспроизведения элемента мультимедиа из текущего списка воспроизведения. Элемент для воспроизведения выбирается в зависимости от его позиции в списке воспроизведения. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Аксвиндовсмедиаплайер. Куррентплайлист (VB и C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. URL (VB и C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Play (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. Item (VB и C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Автозапуск (VB и C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





