---
title: Метод Фетчрепортфаиледперусерентриес класса Win32_TSLicenseReport
description: Получение сведений о неудачных службы удаленных рабочих столов клиентских лицензиях для каждого пользователя (RDS \ 160; CAL на пользователя) из отчета.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортфаиледперусерентриес
- Службы удаленных рабочих столов метода Фетчрепортфаиледперусерентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортфаиледперусерентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4d78ff13ff58f7e80c1f177728ded24dc98588b0a0fb25c3976e9dcc19fdc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737634"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a>Метод Фетчрепортфаиледперусерентриес \_ класса Win32 тслиценсерепорт

Получает сведения о неудачных службы удаленных рабочих столов клиентских лицензиях на клиентские лицензии (RDS на пользователя) из отчета.

## <a name="syntax"></a>Синтаксис


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
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

Число записей отчета, извлекаемых из объекта отчета. Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* . При возврате содержит количество записей в массиве *репортфаиледперусерентриес* .

</dd> <dt>

*Репортфаиледперусерентриес* \[ заполняет\]
</dt> <dd>

Массив классов [**Win32 \_ тслиценсерепортфаиледперусерентри**](win32-tslicensereportfailedperuserentry.md) , представляющих полученные записи лицензий. Параметр *Count* содержит количество элементов в этом массиве.

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

 

 





