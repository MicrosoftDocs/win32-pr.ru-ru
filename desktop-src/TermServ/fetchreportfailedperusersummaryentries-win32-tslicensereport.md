---
title: Метод Фетчрепортфаиледперусерсуммарентриес класса Win32_TSLicenseReport
description: Получение сводных данных о неудачных службы удаленных рабочих столов клиентских лицензиях для каждого пользователя (RDS \ 160; CAL на пользователя) из отчета.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортфаиледперусерсуммарентриес
- Службы удаленных рабочих столов метода Фетчрепортфаиледперусерсуммарентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортфаиледперусерсуммарентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc42cb36ad0d203389dd115eb6bf02b1135982f1c490a0f669e19d2f64e937ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737554"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>Метод Фетчрепортфаиледперусерсуммарентриес \_ класса Win32 тслиценсерепорт

Получение сводных данных о неудачных службы удаленных рабочих столов клиентских лицензиях на клиентские лицензии (RDS на пользователя) из отчета.

## <a name="syntax"></a>Синтаксис


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
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

Число записей отчета, извлекаемых из объекта отчета. Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* . При возврате содержит количество записей в массиве *репортфаиледперусерсуммарентриес* .

</dd> <dt>

*Репортфаиледперусерсуммарентриес* \[ заполняет\]
</dt> <dd>

Массив классов [**Win32 \_ тслиценсерепортфаиледперусерсуммарентри**](win32-tslicensereportfailedperusersummaryentry.md) , представляющих полученные записи лицензий. Параметр *Count* содержит количество элементов в этом массиве.

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

 

 





