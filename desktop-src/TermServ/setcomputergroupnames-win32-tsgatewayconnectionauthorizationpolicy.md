---
title: Метод Сеткомпутерграупнамес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Компутерграупнамес.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеткомпутерграупнамес
- Службы удаленных рабочих столов метода Сеткомпутерграупнамес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сеткомпутерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415440"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Сеткомпутерграупнамес \_ класса Win32 тсгатевайконнектионаусоризатионполици

Задает свойство **компутерграупнамес** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Компутерграупнамес* \[ окне\]
</dt> <dd>

Список имен групп компьютеров, разделенных точкой с запятой. Это значение может быть пустым. Имена имеют формат *домена \\ компутерграупнаме*. Если указано значение, клиентский компьютер должен принадлежать к одной из этих групп компьютеров, чтобы пользователь был доступен на сервере шлюза удаленных рабочих столов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Если в параметре *компутерграупнамес* указано несколько имен групп компьютеров и одно из имен не может быть обработано, никакие имена не будут обработаны.

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

