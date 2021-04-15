---
title: IWMPStringCollection2 Жетитеминфобитипе, метод
description: Метод Жетитеминфобитипе возвращает значение, соответствующее указанному индексу элемента коллекции строк, имени, языку и индексу атрибута.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- Жетитеминфобитипе метод Windows Media Player
- Жетитеминфобитипе метод проигрывателя Windows Media Player, интерфейс IWMPStringCollection2
- Интерфейс IWMPStringCollection2 Windows Media Player, метод Жетитеминфобитипе
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708466"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>Метод IWMPStringCollection2:: Жетитеминфобитипе

Метод **жетитеминфобитипе** возвращает значение, соответствующее указанному индексу элемента коллекции строк, имени, языку и индексу атрибута.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*лколлектиониндекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , являющийся начинающимся с нуля индексом элемента коллекции строк, из которого необходимо получить атрибут.

</dd> <dt>

*бстртипе* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем атрибута.

</dd> <dt>

*бстрлангуаже* \[ окне\]
</dt> <dd>

**Строка System. String** , указывающая язык. Если задано значение null или строка нулевой длины (""), используется текущая строка языкового стандарта. В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".

</dd> <dt>

*латтрибутеиндекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , который является индексом атрибута (начинающийся с нуля).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект **System. Object** , являющийся элементом коллекции строк.

## <a name="remarks"></a>Комментарии

Этот метод поддерживает атрибуты с несколькими значениями и атрибутами со сложными значениями. Метод **getItemInfo** не поддерживает атрибуты с несколькими значениями или атрибутами со сложными значениями.

Передав значение "Чилдлист" в параметре *бстртипе* , можно получить новую коллекцию строк, содержащую дочерние элементы одного из элементов в родительской коллекции строк. Например, если родительская коллекция содержит список Албумидс, этот метод можно использовать для получения коллекции дочерних строк, содержащей все дорожки для одного из альбомов. Этот подход быстрее и эффективнее, чем вызов метода **IWMPMediaCollection2. жетстрингколлектионбикуери** дважды; один раз для получения коллекции Албумидс и второй раз для получения коллекции дорожек для определенного Албумид. Чтобы использовать Чилдлист только что описанным способом, родительская коллекция строк должна быть получена из коллекции носителей через **ивмплибрарисервицес**, а не с помощью свойства **аксвиндовсмедиаплайер. медиаколлектион** .

При использовании Чилдлист передайте значение "Чилдлист" в параметре *бстртипе* и значение 0 в параметре *латтрибутеиндекс* . Затем можно привести объект, возвращаемый к интерфейсу **IWMPStringCollection2** , для доступа к дочернему списку.

Чтобы использовать этот метод, необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Атрибут Албумид**](albumid-attribute.md)
</dt> <dt>

[**Интерфейс Ивмплибрарисервицес (VB и C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. Жетстрингколлектионбикуери (VB и C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPStringCollection2**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfo (VB и C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





