---
title: Аксвиндовсмедиаплайер. Куррентмедиа, свойство
description: Свойство Куррентмедиа Возвращает или задает интерфейс Ивмпмедиа, соответствующий текущему элементу мультимедиа.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- Проигрыватель Windows Media для свойства Куррентмедиа
- Куррентмедиа свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Куррентмедиа
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698952"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a>Аксвиндовсмедиаплайер. Куррентмедиа, свойство

Свойство Куррентмедиа Возвращает или задает интерфейс Ивмпмедиа, соответствующий текущему элементу мультимедиа.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a>Значение свойства

Интерфейс Вмплиб. Ивмпмедиа, предоставляющий доступ к текущему элементу мультимедиа.

## <a name="remarks"></a>Комментарии

Если Аксвиндовсмедиаплайер. Settings. Свойство **автозапуска** имеет значение true, воспроизведение начинается автоматически при установке **куррентмедиа**.

Интерфейс Ивмпмедиа для данного элемента мультимедиа можно получить с помощью свойства Ивмпплайлист. Item (метод Ивмпплайлист. Get \_ Item в C#). Чтобы загрузить элемент мультимедиа с помощью имени файла, задайте свойство URL-адреса или используйте Невмедиа.

## <a name="examples"></a>Примеры

В следующем примере извлекается первый элемент мультимедиа из библиотеки и используется свойство Куррентмедиа, чтобы задать полученный элемент мультимедиа в качестве текущего элемента мультимедиа и отобразить его имя. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. Невмедиа (VB и C#)**](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. URL (VB и C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. Item (VB и C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Автозапуск (VB и C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





