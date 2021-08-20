---
title: Метод Ремоветскграуп класса Win32_TSLicenseServer
description: Ремоветскграуп больше не доступен для использования в Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремоветскграуп
- Службы удаленных рабочих столов метода Ремоветскграуп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ремоветскграуп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebcd3c0eacb54a14675d2794f1c42f8e7a18cd9ea78c7f6369ef883cc3d9fad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127509"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a>Метод Ремоветскграуп \_ класса Win32 тслиценсесервер

\[**Ремоветскграуп** больше не доступен для использования в Windows Server 2012.\]

Этот метод не поддерживается.

**Windows server 2008 R2 и Windows server 2008:** Удаляет локальную группу "компьютеры сервера терминалов" с сервера лицензий удаленный рабочий стол.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **WBEM \_ E \_ не \_ поддерживается**.

**Windows server 2008 R2 и Windows server 2008:** Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

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
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> <dt>

[**истскграуппресент**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

