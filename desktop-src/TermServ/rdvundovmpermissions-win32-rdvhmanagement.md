---
title: Метод Рдвундовмпермиссионс класса Win32_RdvhManagement
description: Отмена разрешений, установленных Рдвсетупвмпермиссионс на указанной виртуальной машине.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвундовмпермиссионс
- Службы удаленных рабочих столов метода Рдвундовмпермиссионс, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвундовмпермиссионс
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492759"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Метод Рдвундовмпермиссионс \_ класса Win32 рдвхманажемент

Отмена разрешений, установленных [**рдвсетупвмпермиссионс**](rdvsetupvmpermissions-win32-rdvhmanagement.md) на указанной виртуальной машине.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*VmName* \[ окне\]
</dt> <dd>

Имя виртуальной машины для отмены разрешений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                             |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                   |
| MOF<br/>                      | <dl> <dt>Тсвмхост. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдвхманажемент Win32**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





