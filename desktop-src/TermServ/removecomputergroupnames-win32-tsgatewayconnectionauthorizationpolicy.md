---
title: Метод Ремовекомпутерграупнамес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Удаляет указанные имена групп компьютеров из свойства Компутерграупнамес.
ms.assetid: 5f4e566a-1a2e-459d-ab6c-53ffd42271d8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовекомпутерграупнамес
- Службы удаленных рабочих столов метода Ремовекомпутерграупнамес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Ремовекомпутерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ec281798fba0257883eebfb60ac199b0f3c1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071399"
---
# <a name="removecomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Ремовекомпутерграупнамес \_ класса Win32 тсгатевайконнектионаусоризатионполици

Удаляет указанные имена групп компьютеров из свойства **компутерграупнамес** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Компутерграупнамес* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список имен групп компьютеров, которые нужно удалить из свойства **компутерграупнамес** . Имена групп компьютеров должны иметь формат *домена \\ компутерграупнаме*.

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

 

