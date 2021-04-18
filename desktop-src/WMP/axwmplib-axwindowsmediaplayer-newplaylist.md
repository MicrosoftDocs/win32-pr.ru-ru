---
title: Аксвиндовсмедиаплайер. Невплайлист, метод
description: Метод Невплайлист возвращает интерфейс Ивмпплайлист для нового списка воспроизведения.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- Невплайлист метод Windows Media Player
- Невплайлист метод Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, метод Невплайлист
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698765"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a>Аксвиндовсмедиаплайер. Невплайлист, метод

Метод Невплайлист возвращает интерфейс Ивмпплайлист для нового списка воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*bstrName* 
</dt> <dd>

**Строка System. String** , которая является именем нового списка воспроизведения.

</dd> <dt>

*бструрл* 
</dt> <dd>

**Строка System. String** , которая является URL-адресом списка воспроизведения метафайла Windows Media, который используется для инициализации нового списка воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс Вмплиб. Ивмпплайлист, представляющий только что созданный список воспроизведения.

## <a name="remarks"></a>Комментарии

Если параметр *бструрл* имеет значение null или является строкой нулевой длины (""), этот метод создает пустой **список воспроизведения**. Если параметр *bstrName* является строкой нулевой длины (""), этот метод применяет текущее имя метафайла.

Новый список воспроизведения, созданный с помощью этого метода, не добавляется в библиотеку. Чтобы добавить новый список воспроизведения в библиотеку, используйте Ивмпплайлистколлектион. **импортплайлист** или ивмпплайлистколлектион. **невплайлист**. Все начальные и конечные пробелы в имени списка воспроизведения автоматически удаляются при добавлении в библиотеку.

Так как библиотека допускает наличие нескольких списков воспроизведения с одинаковыми именами, перед добавлением нового списка воспроизведения может потребоваться проверить, есть ли у него указанное имя.

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

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Импортплайлист (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Невплайлист (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





