---
title: Метод Сетенаблед класса Win32_TSGatewayResourceAuthorizationPolicy
description: Включает или отключает политику авторизации ресурсов удаленный рабочий стол (RD \ 160; RAP) путем установки свойства Enabled.
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетенаблед
- Службы удаленных рабочих столов метода Сетенаблед, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Сетенаблед
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de7c4e013690a5d5e8ffd6b235a42ea43c445ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492753"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Метод Сетенаблед \_ класса Win32 тсгатевайресаурцеаусоризатионполици

Включает или отключает политику авторизации ресурсов (RD RAP) удаленный рабочий стол, устанавливая свойство **Enabled** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Включено* \[ окне\]
</dt> <dd>

Если задано **значение true**, то политика авторизации ресурсов удаленных рабочих столов будет включена. Если задано **значение false**, политика авторизации ресурсов удаленных рабочих столов будет отключена.

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

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

