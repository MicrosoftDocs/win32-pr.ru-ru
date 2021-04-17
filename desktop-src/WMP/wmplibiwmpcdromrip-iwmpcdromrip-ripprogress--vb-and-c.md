---
title: Ивмпкдромрип Риппрогресс, свойство
description: Свойство Риппрогресс получает сведения о ходе копирования компакт-диска в процентах завершения.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- Проигрыватель Windows Media для свойства Риппрогресс
- Риппрогресс свойство проигрывателя Windows Media Player, интерфейс Ивмпкдромрип
- Интерфейс Ивмпкдромрип Windows Media Player, свойство Риппрогресс
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717955"
---
# <a name="iwmpcdromripripprogress-property"></a>Свойство Ивмпкдромрип:: Риппрогресс

Свойство **риппрогресс** получает сведения о ходе копирования компакт-диска в процентах завершения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является значением хода выполнения. Значения хода выполнения находятся в диапазоне от 0 до 100.

## <a name="remarks"></a>Комментарии

Значение Progress представляет завершенный процент всего процесса копирования. Чтобы определить ход выполнения определенной записи, используйте [ивмпмедиа. getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) с **риппрогресс** в качестве имени атрибута. Чтобы получить индекс дорожки, скопированной в данный момент, вызовите Ивмпплайлист. getItemInfo с именем атрибута "Куррентриптраккиндекс".

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпкдромрип (VB и C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Копирование компакт-диска**](ripping-a-cd.md)
</dt> </dl>

 

 





