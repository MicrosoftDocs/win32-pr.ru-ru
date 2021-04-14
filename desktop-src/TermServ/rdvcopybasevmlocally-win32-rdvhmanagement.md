---
title: Метод Рдвкопибасевмлокалли класса Win32_RdvhManagement
description: Копирует локальную базовую виртуальную машину на указанный сервер узла виртуализации удаленных рабочих столов (RDV).
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвкопибасевмлокалли
- Службы удаленных рабочих столов метода Рдвкопибасевмлокалли, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвкопибасевмлокалли
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416045"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a>Метод Рдвкопибасевмлокалли \_ класса Win32 рдвхманажемент

Копирует локальную базовую виртуальную машину на указанный сервер узла виртуализации удаленных рабочих столов (RDV).

## <a name="syntax"></a>Синтаксис


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Басевмлокатион* \[ окне\]
</dt> <dd>

Расположение базовой виртуальной машины.

</dd> <dt>

*Фармнаме* \[ окне\]
</dt> <dd>

Имя фермы узлов, в которую производится копирование.

</dd> <dt>

*Голдкачелокатион* \[ окне\]
</dt> <dd>

Расположение кэша Gold.

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

 

 





