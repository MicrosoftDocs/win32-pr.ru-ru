---
title: Метод Ислспублишед класса Win32_TSLicenseServer
description: Возвращает значение, указывающее, опубликован ли сервер лицензий удаленный рабочий стол в службах домен Active Directory Services (AD \ 160; DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ислспублишед
- Службы удаленных рабочих столов метода Ислспублишед, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ислспублишед
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672719"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a>Метод Ислспублишед \_ класса Win32 тслиценсесервер

Возвращает значение, указывающее, опубликован ли сервер лицензирования удаленный рабочий стол в службах домен Active Directory Services (AD DS).

## <a name="syntax"></a>Синтаксис


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дата публикации* \[ заполняет\]
</dt> <dd>

Логическое значение, указывающее, опубликован ли сервер лицензирования в AD DS.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Если сервер лицензирования опубликован в AD DS, он будет автоматически обнаруживаться удаленный рабочий стол серверами узлов сеансов удаленных рабочих столов в том же лесу.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

