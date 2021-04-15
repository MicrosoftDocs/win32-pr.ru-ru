---
title: Метод Регистерлстоскп класса Win32_TSLicenseServer
description: Регистрирует сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.
ms.assetid: F0519C8C-49A9-40B1-88DB-FD0419469E62
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Регистерлстоскп
- Службы удаленных рабочих столов метода Регистерлстоскп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Регистерлстоскп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RegisterLSToSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f744109fd26f7dfdf3d5d7f8442470a49adbaf71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489351"
---
# <a name="registerlstoscp-method-of-the-win32_tslicenseserver-class"></a>Метод Регистерлстоскп \_ класса Win32 тслиценсесервер

Регистрирует сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RegisterLSToSCP();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                         |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

