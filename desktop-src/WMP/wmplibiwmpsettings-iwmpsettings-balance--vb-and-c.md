---
title: Свойство баланса Ивмпсеттингс
description: Свойство Balance получает или задает текущее значение стерео баланса.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- проигрыватель Windows Media свойства баланса
- свойство balance проигрыватель Windows Media, интерфейс ивмпсеттингс
- интерфейс ивмпсеттингс проигрыватель Windows Media, свойство balance
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
ms.openlocfilehash: 76d519d656be6b4974e2b4dd2707aafb2bb153f6b26bafe75de948d5e50c67b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861090"
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

## <a name="remarks"></a>Remarks

Нулевое значение указывает на то, что звук воспроизводится на равном томе как в левом, так и в правой канале. Значение 100 указывает, что звук воспроизводится только в левом канале. Значение 100 указывает, что звук воспроизводится только в правильном канале.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                                                     |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





