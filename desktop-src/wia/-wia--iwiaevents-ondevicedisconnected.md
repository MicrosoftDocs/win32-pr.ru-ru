---
description: событие, возникающее при отключении нового аппаратного устройства для получения Windows изображений (WIA).
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Событие WIA. Ондевицедисконнектед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b9d61d196e3a9a7471b9a1fb1ab86c3ba918427ccc5dd5060ffaabdf28f80871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442160"
---
# <a name="wiaondevicedisconnected-event"></a>Событие WIA. Ондевицедисконнектед

событие, возникающее при отключении нового аппаратного устройства для получения Windows изображений (WIA).

## <a name="syntax"></a>Синтаксис


```JScript
Wia.OnDeviceDisconnected(
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

WIA уведомляет сценарий или приложение каждый раз при отключении аппаратного устройства от компьютера. Реализуйте  \_ подпрограммы обжвиа **ондевицедисконнектед ()** , чтобы разрешить сценарию или приложению отвечать на отключение устройства.

Например, может потребоваться, чтобы скрипт обновлял коллекцию [**устройств**](-wia-iwia-devices.md) при удалении устройства с компьютера.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




