---
title: Метод Рдвсетупвмпермиссионс класса Win32_RdvhManagement
description: Устанавливает разрешения на виртуальную машину для текущего пользователя.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвсетупвмпермиссионс
- Службы удаленных рабочих столов метода Рдвсетупвмпермиссионс, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвсетупвмпермиссионс
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490605"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Метод Рдвсетупвмпермиссионс \_ класса Win32 рдвхманажемент

Устанавливает разрешения на виртуальную машину для текущего пользователя.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*VmName* \[ окне\]
</dt> <dd>

Имя виртуальной машины, для которой нужно задать разрешения.

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

 

 





