---
title: Метод Дисаблепринтерс класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Принтерсдисаблед. Если свойство Девицередиректионтипе имеет значение \ 0034; 2 \ 0034;, свойство Принтерсдисаблед управляет перенаправлением принтеров для сеансов, установленных с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: bf58d226-e3de-4c2b-aaa9-9e7ddbf49d31
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисаблепринтерс
- Службы удаленных рабочих столов метода Дисаблепринтерс, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Дисаблепринтерс
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePrinters
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625425170bd5e29b953db8299048261e9351bff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672512"
---
# <a name="disableprinters-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Дисаблепринтерс \_ класса Win32 тсгатевайконнектионаусоризатионполици

Задает свойство **принтерсдисаблед** . Если свойство **девицередиректионтипе** имеет значение 2, то свойство **принтерсдисаблед** управляет перенаправлением принтеров для сеансов, которые устанавливаются с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 DisablePrinters(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Отключено* \[ окне\]
</dt> <dd>

Новое значение для свойства **принтерсдисаблед** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

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

 

