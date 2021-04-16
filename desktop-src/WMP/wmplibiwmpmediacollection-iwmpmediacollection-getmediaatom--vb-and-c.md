---
title: Ивмпмедиаколлектион Жетмедиаатом, метод
description: Метод Жетмедиаатом возвращает индекс указанного атрибута в наборе доступных атрибутов.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- Жетмедиаатом метод Windows Media Player
- Жетмедиаатом метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетмедиаатом
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699199"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>Метод Ивмпмедиаколлектион:: Жетмедиаатом

`getMediaAtom`Метод возвращает индекс указанного атрибута в наборе доступных атрибутов.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстритемнаме* \[ окне\]
</dt> <dd>

**Строка System. String** , представляющая собой имя элемента, для которого должен быть получен индекс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Int32** , которое является индексом.

## <a name="remarks"></a>Комментарии

Номер индекса, полученный с помощью этого метода, может быть передан в **ивмпмедиа. жетитеминфобятом** для доступа к значениям атрибута. Эта методика обычно более эффективна при работе с большими списками воспроизведения, чем доступ к значению атрибута по имени с помощью **ивмпмедиа. getItemInfo**.

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмпмедиа. getItemInfo (VB и C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Жетитеминфобятом (VB и C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





