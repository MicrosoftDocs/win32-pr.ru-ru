---
description: событие, возникающее при подключении нового аппаратного устройства для получения Windows изображений (WIA).
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Событие WIA. Ондевицеконнектед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d878cc663cc9f7ea1422e2dc2cad10e652296a48ef597cf699fe5eb3af99e49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209551"
---
# <a name="wiaondeviceconnected-event"></a>Событие WIA. Ондевицеконнектед

событие, возникающее при подключении нового аппаратного устройства для получения Windows изображений (WIA).

## <a name="syntax"></a>Синтаксис


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Id* 
</dt> <dd>

Строка, содержащая идентификатор подключенного устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

WIA уведомляет сценарий или приложение при подключении нового аппаратного устройства к компьютеру. Реализуйте  \_ подпрограммы обжвиа **ондевицеконнектед ()** , чтобы сценарий или приложение отвечало на подключение устройства.

Например, может потребоваться, чтобы скрипт обновлял коллекцию [**устройств**](-wia-iwia-devices.md) при установке нового устройства.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




