---
title: Метод Ислсрегистередтоскп класса Win32_TSLicenseServer
description: Возвращает значение, указывающее, зарегистрирован ли сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.
ms.assetid: 013C3711-7C55-4DB4-9229-C3C60E751EF2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ислсрегистередтоскп
- Службы удаленных рабочих столов метода Ислсрегистередтоскп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ислсрегистередтоскп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSRegisteredToSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47ca9eadbdbaaba49311b212e83528ee391387e7aca1512a1ab0001a2bbae8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058342"
---
# <a name="islsregisteredtoscp-method-of-the-win32_tslicenseserver-class"></a>Метод Ислсрегистередтоскп \_ класса Win32 тслиценсесервер

Возвращает значение, указывающее, зарегистрирован ли сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.

## <a name="syntax"></a>Синтаксис


```mof
uint32 IsLSRegisteredToSCP(
  [out] boolean Registered
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Зарегистрировано* \[ заполняет\]
</dt> <dd>

Логическое значение, указывающее, зарегистрирован ли сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

