---
title: IWMPStringCollection2 getItemInfo, метод
description: Метод getItemInfo возвращает строку, соответствующую указанному индексу и имени элемента коллекции строк.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод проигрывателя Windows Media Player, интерфейс IWMPStringCollection2
- Интерфейс IWMPStringCollection2 Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708467"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a>Метод IWMPStringCollection2:: getItemInfo

Метод **getItemInfo** возвращает строку, соответствующую указанному индексу и имени элемента коллекции строк.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*лколлектиониндекс* \[ окне\]
</dt> <dd>

Значение **System. Int32** , указывающее Отсчитываемый от нуля индекс элемента коллекции строк, из которого необходимо получить атрибут.

</dd> <dt>

*бстритемнаме* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая является именем элемента коллекции строк. Для атрибутов, базовым значением которых является **System. Boolean**, возвращается строка «true» или «false».

## <a name="remarks"></a>Комментарии

Чтобы получить атрибуты с несколькими значениями и атрибутами со сложными значениями, используйте метод **жетитеминфобитипе** .

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPStringCollection2**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. Жетитеминфобитипе (VB и C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





