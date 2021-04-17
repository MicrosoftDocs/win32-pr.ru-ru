---
description: Указывает состояние работоспособности приложения.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: Перечисление APPLICATION_STATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663383"
---
# <a name="application_state-enumeration"></a>\_Перечисление состояния приложения

Указывает состояние работоспособности приложения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**аппликатионстатехеалси**
</dt> <dd>

Приложение находится в работоспособном состоянии.

</dd> <dt>

<span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**аппликатионстатекритикал**
</dt> <dd>

Состояние приложения является критическим.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы использовать этот программный элемент, на виртуальной машине, в которой выполняется приложение, должны быть установлены компоненты интеграции Windows 8.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                                |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                      |
| Версия<br/>                  | Компоненты интеграции для Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>Вмаппликатионхеалсмонитор. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сетаппликатионстате**](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




