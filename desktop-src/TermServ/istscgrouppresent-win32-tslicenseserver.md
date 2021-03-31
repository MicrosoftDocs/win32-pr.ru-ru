---
title: Метод Истскграуппресент класса Win32_TSLicenseServer
description: Истскграуппресент больше не доступен для использования в Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Истскграуппресент
- Службы удаленных рабочих столов метода Истскграуппресент, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Истскграуппресент
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071401"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a>Метод Истскграуппресент \_ класса Win32 тслиценсесервер

\[**Истскграуппресент** больше не доступен для использования в Windows Server 2012.\]

Этот метод не поддерживается.

**Windows server 2008 R2 и Windows server 2008:** Возвращает значение, указывающее, существует ли локальная группа компьютеров сервера терминалов на удаленный рабочий стол сервере лицензирования.

## <a name="syntax"></a>Синтаксис


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имеется* \[ заполняет\]
</dt> <dd>

Логическое значение, указывающее, существует ли локальная группа компьютеров сервера терминалов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **WBEM \_ E \_ не \_ поддерживается**.

**Windows server 2008 R2 и Windows server 2008:** Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>                                                                 |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                                                         |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

