---
description: 'Метод Ипортабледевицевалуесколлектион:: Add — метод Add добавляет элемент в коллекцию.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'Метод Ипортабледевицевалуесколлектион:: Add (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083249"
---
# <a name="iportabledevicevaluescollectionadd-method"></a>Метод Ипортабледевицевалуесколлектион:: Add

Метод **Add** добавляет элемент в коллекцию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвалуес* \[ окне\]
</dt> <dd>

Указатель на интерфейс **ипортабледевицевалуес** для добавления в коллекцию. Интерфейс на самом деле не копируется, но на нем вызывается метод **AddRef** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                   | Описание                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Метод выполнен успешно.<br/>                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для добавления значения в коллекцию.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуесколлектион**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




