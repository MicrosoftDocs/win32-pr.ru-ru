---
title: Метод Фетчрепортсуммарентриес класса Win32_TSLicenseReport
description: Извлекает сводные данные по клиентским лицензиям службы удаленных рабочих столов на пользователя (RDS \ 160; CAL на пользователя) из отчета.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортсуммарентриес
- Службы удаленных рабочих столов метода Фетчрепортсуммарентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортсуммарентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094d7fe1f7aa3d5acabce7d7d248c16601b5005d09f2583cc23c7390c3642361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348579"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a>Метод Фетчрепортсуммарентриес \_ класса Win32 тслиценсерепорт

Возвращает сводные данные о лицензиях на клиентский доступ службы удаленных рабочих столов на пользователя (клиентские лицензии RDS на пользователя) из отчета.

## <a name="syntax"></a>Синтаксис


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*StartIndex* \[ окне\]
</dt> <dd>

Индекс первой записи отчета, которая должна быть получена. Первая запись отчета имеет нулевой индекс.

</dd> <dt>

*Количество* \[ в, out\]
</dt> <dd>

Число записей отчета, извлекаемых из объекта отчета. Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* . При возврате содержит количество записей в массиве *репортсуммарентриес* .

</dd> <dt>

*Репортсуммарентриес* \[ заполняет\]
</dt> <dd>

Возвращает массив классов [**Win32 \_ тслиценсерепортсуммарентри**](win32-tslicensereportsummaryentry.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Значение **лсервер \_ I \_ \_ unmore \_ Data** (0x4001) означает, что больше нет записей отчетов.

## <a name="remarks"></a>Remarks

Это не статический метод. Этот метод должен вызываться из объекта отчета об использовании лицензий на пользователя.

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тслиценсерепорт Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_Тслиценсерепортсуммарентри Win32**](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

