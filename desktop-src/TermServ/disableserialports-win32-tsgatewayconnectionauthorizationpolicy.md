---
title: Метод Дисаблесериалпортс класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Сериалпортсдисаблед.
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисаблесериалпортс
- Службы удаленных рабочих столов метода Дисаблесериалпортс, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Дисаблесериалпортс
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a4f6941f8bc98d7f8e424a984922ad1f6631c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801462"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Дисаблесериалпортс \_ класса Win32 тсгатевайконнектионаусоризатионполици

Задает свойство **сериалпортсдисаблед** . Если свойство **девицередиректионтипе** имеет значение 2, то свойство **сериалпортсдисаблед** управляет перенаправлением последовательных портов для сеансов, установленных с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Отключено* \[ окне\]
</dt> <dd>

Новое значение для свойства **сериалпортсдисаблед** .

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

 

