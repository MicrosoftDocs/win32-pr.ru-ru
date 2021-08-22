---
title: Метод Фетчрепортпердевицеентриес класса Win32_TSLicenseReport
description: Получение сведений о выданных лицензиях на клиентский доступ службы удаленных рабочих столов на устройство (RDS \ 160; CAL "на устройство") из отчета.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортпердевицеентриес
- Службы удаленных рабочих столов метода Фетчрепортпердевицеентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортпердевицеентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3a5ef050002da069f7eda56352f204797cac521885248bc7e63dfd77f840f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737564"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a>Метод Фетчрепортпердевицеентриес \_ класса Win32 тслиценсерепорт

Получение сведений о выданных лицензиях на клиентский доступ службы удаленных рабочих столов для каждого устройства (клиентские лицензии служб удаленных рабочих столов на устройство) из отчета.

## <a name="syntax"></a>Синтаксис


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*StartIndex* \[ окне\]
</dt> <dd>

Индекс первой записи отчета для извлечения. Первая запись отчета имеет нулевой индекс.

</dd> <dt>

*Количество* \[ в, out\]
</dt> <dd>

Число записей отчета, извлекаемых из объекта отчета. Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* . При возврате содержит количество записей в массиве *репортпердевицеентриес* .

</dd> <dt>

*Репортпердевицеентриес* \[ заполняет\]
</dt> <dd>

Массив классов [**Win32 \_ тслиценсерепортпердевицеентри**](win32-tslicensereportperdeviceentry.md) , представляющих полученные записи лицензий. Параметр *Count* содержит количество элементов в этом массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тслиценсерепорт Win32**](win32-tslicensereport.md)
</dt> </dl>

 

 





