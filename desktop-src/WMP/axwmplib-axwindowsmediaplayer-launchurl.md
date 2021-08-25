---
title: Аксвиндовсмедиаплайер. Лаунчурл, метод
description: Метод Лаунчурл отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру. | Аксвиндовсмедиаплайер. Лаунчурл, метод
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- проигрыватель Windows Media метода лаунчурл
- проигрыватель Windows Media метода лаунчурл, класс аксвиндовсмедиаплайер
- класс аксвиндовсмедиаплайер проигрыватель Windows Media, метод лаунчурл
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
ms.openlocfilehash: 3b4f3ad10a6defe4e7db252a1703888550ff5a89fe2a0d0618dd9886fc5f74bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123994"
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

## <a name="remarks"></a>Remarks

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
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





