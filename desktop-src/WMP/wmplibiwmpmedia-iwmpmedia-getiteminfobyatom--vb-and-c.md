---
title: Ивмпмедиа Жетитеминфобятом, метод
description: Метод Жетитеминфобятом возвращает значение атрибута с указанным номером индекса.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- Жетитеминфобятом метод Windows Media Player
- Жетитеминфобятом метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод Жетитеминфобятом
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669255"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>Метод Ивмпмедиа:: Жетитеминфобятом

Метод **жетитеминфобятом** возвращает значение атрибута с указанным номером индекса.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*Латом* \[ окне\]
</dt> <dd>

Объект **System. Int32** , указывающий индекс, в котором запрошенный атрибут находится в наборе доступных атрибутов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая является значением атрибута.

## <a name="remarks"></a>Комментарии

Этот метод можно использовать для получения метаданных для определенного элемента мультимедиа с помощью номера индекса атрибута. Свойство **аттрибутекаунт** можно использовать для определения количества атрибутов, доступных для элемента мультимедиа.

Метод **жетмедиаатом** интерфейса **ивмпмедиаколлектион** также можно использовать для получения индекса определенного атрибута. Этот метод, как правило, более эффективен, чем методы **getItemInfo** или **жетитеминфобитипе** при работе с большими списками воспроизведения.

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Аттрибутекаунт (VB и C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. getItemInfo (VB и C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Сетитеминфо (VB и C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. Жетитеминфобитипе (VB и C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиаколлектион. Жетмедиаатом (VB и C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





