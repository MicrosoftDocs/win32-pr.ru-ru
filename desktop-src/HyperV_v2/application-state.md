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
ms.openlocfilehash: 5f873e7a30a4cff6dc4cc89eaea225201a367f7c24ead11ad95da04c2ff1ab32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914164"
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

## <a name="remarks"></a>Remarks

чтобы использовать этот программный элемент, на виртуальной машине, в которой выполняется приложение, должны быть установлены компоненты интеграции Windows 8.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                      |
| Версия<br/>                  | Интеграционные компоненты для Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>Вмаппликатионхеалсмонитор. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сетаппликатионстате**](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




