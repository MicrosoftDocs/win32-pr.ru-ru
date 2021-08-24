---
title: Метод Сетсекуреидалловед класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Этот метод зарезервирован для использования в будущем.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсекуреидалловед
- Службы удаленных рабочих столов метода Сетсекуреидалловед, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетсекуреидалловед
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99039cd541ad8ab1746ace55de13f35722ea1ba7ccf52fd1a3de93e39e56798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865114"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Сетсекуреидалловед \_ класса Win32 тсгатевайконнектионаусоризатионполици

Этот метод зарезервирован для использования в будущем.

Задает свойство **секуреидалловед** , которое зарезервировано для использования в будущем.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Разрешено* \[ окне\]
</dt> <dd>

Новое значение **секуреидалловед** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

