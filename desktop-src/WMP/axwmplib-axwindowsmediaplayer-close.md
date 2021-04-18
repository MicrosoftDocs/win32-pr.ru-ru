---
title: Аксвиндовсмедиаплайер. Close, метод
description: Метод Close закрывает текущий файл мультимедиа, останавливает воспроизведение в проигрывателе Windows Media и освобождает ресурсы проигрывателя Windows Media.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- закрыть метод проигрыватель Windows Media Player
- закрыть метод проигрыватель Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер проигрыватель Windows Media Player, метод Close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694908"
---
# <a name="axwindowsmediaplayerclose-method"></a>Аксвиндовсмедиаплайер. Close, метод

Метод Close закрывает текущий файл мультимедиа, останавливает воспроизведение в проигрывателе Windows Media и освобождает ресурсы проигрывателя Windows Media.

## <a name="syntax"></a>Синтаксис


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод закрывает текущий файл мультимедиа, а не проигрыватель Windows Media.

## <a name="examples"></a>Примеры

В следующем примере создается кнопка, которая при нажатии останавливает воспроизведение в проигрывателе Windows Media и освобождает используемые ресурсы. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
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
</dt> </dl>

 

 





