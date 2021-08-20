---
title: Ивмпмедиа Жетитеминфобятом, метод
description: Метод Жетитеминфобятом возвращает значение атрибута с указанным номером индекса.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- проигрыватель Windows Media метода жетитеминфобятом
- проигрыватель Windows Media метода жетитеминфобятом, интерфейс ивмпмедиа
- проигрыватель Windows Media интерфейса ивмпмедиа, метод жетитеминфобятом
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
ms.openlocfilehash: 72a8820618b39418aa7be82faeef15a372e0e0f90c0db025e99c55be49d8c13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115701"
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

## <a name="remarks"></a>Remarks

Этот метод можно использовать для получения метаданных для определенного элемента мультимедиа с помощью номера индекса атрибута. Свойство **аттрибутекаунт** можно использовать для определения количества атрибутов, доступных для элемента мультимедиа.

Метод **жетмедиаатом** интерфейса **ивмпмедиаколлектион** также можно использовать для получения индекса определенного атрибута. Этот метод, как правило, более эффективен, чем методы **getItemInfo** или **жетитеминфобитипе** при работе с большими списками воспроизведения.

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 





