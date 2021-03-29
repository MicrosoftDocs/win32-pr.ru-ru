---
title: Метод Женератерепортекс класса Win32_TSLicenseReport
description: Создает отчет о текущем использовании лицензий для лицензий "на пользователя" и "на устройство".
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Женератерепортекс
- Службы удаленных рабочих столов метода Женератерепортекс, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Женератерепортекс
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414932"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a>Метод Женератерепортекс \_ класса Win32 тслиценсерепорт

Создает отчет о текущем использовании лицензий для лицензий "на пользователя" и "на устройство".

## <a name="syntax"></a>Синтаксис


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя файла* \[ заполняет\]
</dt> <dd>

Имя файла созданного отчета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Это статический метод.

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

