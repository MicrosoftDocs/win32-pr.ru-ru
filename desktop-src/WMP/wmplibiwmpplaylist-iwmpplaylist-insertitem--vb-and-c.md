---
title: Ивмпплайлист insertItem, метод
description: Метод insertItem вставляет элемент мультимедиа в указанном месте в списке воспроизведения.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- проигрыватель Windows Media метода insertItem
- проигрыватель Windows Media метода insertItem, интерфейс ивмпплайлист
- проигрыватель Windows Media интерфейса ивмпплайлист, метод insertItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10717c0891443aaa663b748be6a0cb57e04e58b96beb91db6b02b2f6a4b5b621
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464934"
---
# <a name="iwmpplaylistinsertitem-method"></a>Метод Ивмпплайлист:: insertItem

Метод **insertItem** вставляет элемент мультимедиа в указанном месте в списке воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*Линдекс* \[ окне\]
</dt> <dd>

Значение **System. Int32** , представляющее собой отсчитываемый от нуля индекс, по которому элемент мультимедиа будет вставлен в список воспроизведения.

</dd> <dt>

*пивмпмедиа* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмпмедиа** , представляющий вставляемый элемент мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Индексы всех элементов мультимедиа после вставленного элемента будут увеличены на один.

Перед вызовом этого метода необходимо иметь полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. removeItem (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





