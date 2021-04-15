---
title: Аксвиндовсмедиаплайер. Невмедиа, метод
description: Метод Невмедиа возвращает интерфейс Ивмпмедиа для нового элемента мультимедиа.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- Невмедиа метод Windows Media Player
- Невмедиа метод Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, метод Невмедиа
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695167"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>Аксвиндовсмедиаплайер. Невмедиа, метод

Метод Невмедиа возвращает интерфейс Ивмпмедиа для нового элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бструрл* 
</dt> <dd>

**Строка System. String** , которая является URL-адресом файла цифрового носителя, который используется для инициализации нового элемента мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс Вмплиб. Ивмпмедиа, представляющий только что созданный элемент мультимедиа.

## <a name="remarks"></a>Комментарии

Параметр *бструрл* не должен быть строкой нулевой длины ("") или значением NULL.

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

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





