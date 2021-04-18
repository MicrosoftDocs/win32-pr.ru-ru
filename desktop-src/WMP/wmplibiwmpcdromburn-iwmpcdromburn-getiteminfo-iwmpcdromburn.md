---
title: Ивмпкдромбурн getItemInfo, метод
description: Метод getItemInfo извлекает значение указанного атрибута для компакт-диска.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод проигрывателя Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717981"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>Метод Ивмпкдромбурн:: getItemInfo

Метод **getItemInfo** извлекает значение указанного атрибута для компакт-диска.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстритем* \[ окне\]
</dt> <dd>

**Строка System. String** , которая содержит одно из следующих значений.



| Значение         | Описание                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| аваилаблетиме | Получение времени, доступного на компакт-диске в секундах.                                          |
| Пусто         | Извлекает значение **System. Boolean** (представленное в виде строки), указывающее, является ли компакт-диск пустым. |
| FreeSpace     | Получение свободного места на компакт-диске в байтах.                                                |
| тоталспаце    | Возвращает общее пространство на компакт-диске в байтах.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая является значением указанного атрибута.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11<br/>                                                                                     |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





