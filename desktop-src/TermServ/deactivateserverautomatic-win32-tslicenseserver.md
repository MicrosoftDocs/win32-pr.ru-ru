---
title: Метод Деактиватесервераутоматик класса Win32_TSLicenseServer
description: Деактивирует сервер лицензий удаленный рабочий стол через Интернет.
ms.assetid: 6e049d7f-1753-484d-98b8-fde66d16b5ab
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Деактиватесервераутоматик
- Службы удаленных рабочих столов метода Деактиватесервераутоматик, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Деактиватесервераутоматик
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d466b5f7814d6004bafdd01bce161a481eacf26a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071286"
---
# <a name="deactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Метод Деактиватесервераутоматик \_ класса Win32 тслиценсесервер

Деактивирует сервер лицензий удаленный рабочий стол через Интернет.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DeactivateServerAutomatic(
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

 

