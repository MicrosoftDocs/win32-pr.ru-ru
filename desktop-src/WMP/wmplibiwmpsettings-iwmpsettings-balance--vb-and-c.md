---
title: Свойство баланса Ивмпсеттингс
description: Свойство Balance получает или задает текущее значение стерео баланса.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Свойство баланса проигрыватель Windows Media Player
- Свойство баланса проигрыватель Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Balance
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718029"
---
# <a name="iwmpsettingsbalance-property"></a>Свойство Ивмпсеттингс:: Balance

Свойство **Balance** получает или задает текущее значение стерео баланса.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является значением баланса. Это значение может находиться в диапазоне от 100 до 100. Значение по умолчанию равно нулю.

## <a name="remarks"></a>Комментарии

Нулевое значение указывает на то, что звук воспроизводится на равном томе как в левом, так и в правой канале. Значение 100 указывает, что звук воспроизводится только в левом канале. Значение 100 указывает, что звук воспроизводится только в правильном канале.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                                                     |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





