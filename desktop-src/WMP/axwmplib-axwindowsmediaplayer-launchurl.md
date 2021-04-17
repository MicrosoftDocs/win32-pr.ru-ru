---
title: Аксвиндовсмедиаплайер. Лаунчурл, метод
description: Метод Лаунчурл отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру. | Аксвиндовсмедиаплайер. Лаунчурл, метод
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- Лаунчурл метод Windows Media Player
- Лаунчурл метод Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, метод Лаунчурл
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699026"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a>Аксвиндовсмедиаплайер. Лаунчурл, метод

Метод Лаунчурл отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру.

## <a name="syntax"></a>Синтаксис


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бструрл* 
</dt> <dd>

**Строка System. String** , которая является URL-адресом для запуска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод открывает только веб-страницы с использованием протоколов HTTP или HTTPS.

## <a name="examples"></a>Примеры

В следующем примере создается кнопка, которая при нажатии отображает веб-сайт Майкрософт в новом окне браузера. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

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

 

 





