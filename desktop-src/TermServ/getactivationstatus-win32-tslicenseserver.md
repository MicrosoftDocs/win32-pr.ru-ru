---
title: Метод Жетактиватионстатус класса Win32_TSLicenseServer
description: Возвращает текущее состояние активации сервера лицензирования удаленный рабочий стол.
ms.assetid: 1148ffc5-33c1-41f1-b477-78a5293333d1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетактиватионстатус
- Службы удаленных рабочих столов метода Жетактиватионстатус, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Жетактиватионстатус
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetActivationStatus
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d79daa4c73e95eded95f3c7760eef43f0a01683059cc4974506e7b50f291ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130773"
---
# <a name="getactivationstatus-method-of-the-win32_tslicenseserver-class"></a>Метод Жетактиватионстатус \_ класса Win32 тслиценсесервер

Возвращает текущее состояние активации сервера лицензирования удаленный рабочий стол.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetActivationStatus(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ActivationStatus* \[ заполняет\]
</dt> <dd>

Возвращенное состояние активации может быть одним из следующих.

<dt>

0
</dt> <dd>

Сервер лицензий удаленный рабочий стол активирован.

</dd> <dt>

1
</dt> <dd>

Сервер лицензирования удаленный рабочий стол не активирован.

</dd> <dt>

2
</dt> <dd>

Произошла неизвестная ошибка. Неизвестно, активирован ли сервер лицензий удаленный рабочий стол.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

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

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

