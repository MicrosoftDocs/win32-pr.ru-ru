---
title: Метод Женератерепорт класса Win32_TSLicenseReport (GPMgmt. h)
description: Женератерепорт больше не доступен для использования в Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Женератерепорт
- Службы удаленных рабочих столов метода Женератерепорт, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Женератерепорт
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a619da8130187a4ab5d39de390315dd99b3ee7a171005a4cf66e7bb5677ae87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130783"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>Метод Женератерепорт \_ класса Win32 тслиценсерепорт

\[**Женератерепорт** больше не доступен для использования в Windows Server 2012. Вместо этого используйте [**женератерепортекс**](generatereportex-win32-tslicensereport.md).\]

Этот метод не поддерживается.

**Windows server 2008 R2 и Windows server 2008:** Формирует текущий отчет об использовании лицензий на пользователя на сервере лицензирования удаленный рабочий стол.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Скопетипе* \[ окне\]
</dt> <dd>

Область отчета об использовании лицензий. Он может иметь следующие значения.

<dt>

1
</dt> <dd>

Отчет будет создан для всего домена.

</dd> <dt>

2
</dt> <dd>

Отчет будет создан для подразделения, указанного в параметре *скопевалуе* .

</dd> <dt>

3
</dt> <dd>

Отчет будет создан для всех доверенных доменов.

</dd> </dl> </dd> <dt>

*Скопевалуе* \[ окне\]
</dt> <dd>

Если значение параметра *скопетипе* равно 2, *СКОПЕТИПЕ* указывает подразделение, для которого будет создан отчет. Необходимо указать *скопевалуе* , используя формат **OU =**_OUName1_*_, OU =_*_OUName2_*_..._*.

</dd> <dt>

*Имя файла* \[ заполняет\]
</dt> <dd>

Имя файла созданного отчета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **WBEM \_ E \_ не \_ поддерживается**.

**Windows server 2008 R2 и Windows server 2008:** Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Это статический метод.

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>                                                                 |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                                                         |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| Заголовок<br/>                   | <dl> <dt>GPMgmt. h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тслиценсерепорт Win32**](win32-tslicensereport.md)
</dt> </dl>

 

