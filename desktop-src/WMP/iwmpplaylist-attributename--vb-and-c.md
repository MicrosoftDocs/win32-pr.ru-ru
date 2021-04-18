---
title: Ивмпплайлист. attributeName (VB и C)
description: Свойство attributeName ( \_ метод Get AttributeName в C \) возвращает имя атрибута списка воспроизведения, указанного индексом.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- Проигрыватель Windows Media Ивмпплайлист. attributeName (VB и C)
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685075"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a>Ивмпплайлист. attributeName (VB и C#)

Свойство **attributeName** (метод **Get \_ attributeName** в C#) возвращает имя атрибута списка воспроизведения, указанного индексом.


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a>Параметры

*линдекс*

Объект **System. Int32** , который является индексом атрибута списка воспроизведения.

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая является именем атрибута списка воспроизведения.

## <a name="remarks"></a>Комментарии

**Ивмпплайлист. AttributeName** — это свойство, доступное только для чтения, в Visual Basic, которое принимает параметр, тогда как в C# он называется методом **ивмпплайлист. Get \_ attributeName** .

Число атрибутов, связанных с списком воспроизведения, возвращается свойством **ивмпплайлист. аттрибутекаунт** .

Имя, возвращаемое этим свойством, может быть предоставлено методам **сетитеминфо** или **getItemInfo** для указания или получения значения для именованного атрибута.

Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Дополнительные сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).

## <a name="examples"></a>Примеры

Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. Аттрибутекаунт (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. getItemInfo (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. Сетитеминфо (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





