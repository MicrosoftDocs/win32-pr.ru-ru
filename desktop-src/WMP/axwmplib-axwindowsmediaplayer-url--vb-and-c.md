---
title: Аксвиндовсмедиаплайер. URL, свойство
description: Свойство URL Возвращает или задает имя элемента мультимедиа для воспроизведения.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- проигрыватель Windows Media свойства URL-адреса
- свойство URL-адреса проигрыватель Windows Media, класс аксвиндовсмедиаплайер
- класс аксвиндовсмедиаплайер проигрыватель Windows Media, свойство URL-адреса
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d953f2d85fc1fd83edcd37a491cb2f7cbabc3e3dfaf61e48feb1cd30e6d01934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123884"
---
# <a name="axwindowsmediaplayerurl-property"></a>Аксвиндовсмедиаплайер. URL, свойство

Свойство URL Возвращает или задает имя элемента мультимедиа для воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Значение свойства

Строка System. String, которая является URL-адресом элемента мультимедиа.

## <a name="remarks"></a>Remarks

Этому свойству можно задать только URL-адрес в зоне безопасности с тем же или менее ограниченным, чем зона безопасности вызывающей программы или веб-страницы.

Приложения, которые открывают элементы мультимедиа из защищенного брандмауэра, будут иметь лучшую производительность, если адрес указан с помощью DNS-имени, а не IP-адреса.

Не вызывайте этот метод из кода обработчика событий. Вызов **URL-адреса** из обработчика событий может привести к непредвиденным результатам.

## <a name="examples"></a>Примеры

В следующем примере пользователю предоставляется возможность указать файл мультимедиа, введя путь к файлу в текстовом поле. При нажатии кнопки свойству URL присваивается указанный файл, и файл воспроизводится. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





