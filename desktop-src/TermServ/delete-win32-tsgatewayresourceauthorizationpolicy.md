---
title: Метод Delete класса Win32_TSGatewayResourceAuthorizationPolicy
description: Удаление текущей удаленный рабочий стол политики авторизации ресурсов (RD \ 160; RAP).
ms.assetid: cbabb997-63b8-4a4c-9e16-34f2638fca97
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Delete
- Службы удаленных рабочих столов метода Delete, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad39ebc5cf059575403a86cd790a6350ce520d8864fccc212f5be5a2ae3926b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513493"
---
# <a name="delete-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Метод DELETE \_ класса Тсгатевайресаурцеаусоризатионполици Win32

Удаление текущей удаленный рабочий стол политики авторизации ресурсов (RD RAP).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Delete();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

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

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

