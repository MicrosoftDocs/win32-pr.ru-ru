---
title: Метод Унрегистерлсфромскп класса Win32_TSLicenseServer
description: Удаляет сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.
ms.assetid: 3EE6F272-A99F-49EF-BDED-D8C2C641D45B
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Унрегистерлсфромскп
- Службы удаленных рабочих столов метода Унрегистерлсфромскп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Унрегистерлсфромскп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnRegisterLSFromSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d365b0f3e64c57fba9447d8658c3a955b6e92f73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672611"
---
# <a name="unregisterlsfromscp-method-of-the-win32_tslicenseserver-class"></a>Метод Унрегистерлсфромскп \_ класса Win32 тслиценсесервер

Удаляет сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.

## <a name="syntax"></a>Синтаксис


```mof
uint32 UnRegisterLSFromSCP();
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

 

