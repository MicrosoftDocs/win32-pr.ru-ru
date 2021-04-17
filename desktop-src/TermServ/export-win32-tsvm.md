---
title: Метод Export класса Win32_TSVm
description: Извлекает сведения мониторинга сеанса виртуальной машины.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода экспорта
- Службы удаленных рабочих столов метода экспорта, класс Win32_TSVm
- Win32_TSVm службы удаленных рабочих столов класса, метод Export
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672549"
---
# <a name="export-method-of-the-win32_tsvm-class"></a>Метод Export \_ класса Win32 тсвм

Извлекает сведения мониторинга сеанса виртуальной машины.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Експортфолдерпас* \[ окне\]
</dt> <dd>

Путь к каталогу, в который будет экспортирована виртуальная машина.

</dd> <dt>

*Експортжобобжектпас* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает путь к объекту HyperV Конкретежоб.

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

[**\_Тсвм Win32**](win32-tsvm.md)
</dt> </dl>

 

 





