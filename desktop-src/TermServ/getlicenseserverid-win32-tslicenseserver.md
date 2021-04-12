---
title: Метод Жетлиценсесерверид класса Win32_TSLicenseServer
description: Возвращает идентификатор сервера лицензий удаленный рабочий стол, если сервер активирован в данный момент.
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетлиценсесерверид
- Службы удаленных рабочих столов метода Жетлиценсесерверид, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Жетлиценсесерверид
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a5883a5a52a0d111959e1f9fc1cbe9da5357d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415204"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a>Метод Жетлиценсесерверид \_ класса Win32 тслиценсесервер

Возвращает идентификатор сервера лицензий удаленный рабочий стол, если сервер активирован в данный момент.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*слиценсесерверид* \[ заполняет\]
</dt> <dd>

Идентификатор сервера лицензирования удаленный рабочий стол.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

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

 

