---
title: Метод вниз класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Перемещает текущую политику авторизации подключений удаленный рабочий стол (RD \ 160; CAP) на одну точку вниз в том порядке, в котором RD \ 160; Вычисляются ограничения.
ms.assetid: 57349e59-e200-4789-bbcb-d474eacde39d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода вниз
- Службы удаленных рабочих столов метода вниз, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод вниз
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f401a87445a16fd07d77480bd56bdc904240784d3a7a41e4f7a76a3847f723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058742"
---
# <a name="movedown-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод вниз \_ класса Win32 тсгатевайконнектионаусоризатионполици

Перемещает текущую политику авторизации подключений удаленный рабочий стол (RD CAP) на одну точку вниз в порядке оценки политик удаленных рабочих столов. Этот метод увеличивает свойство **Order** текущей политики авторизации подключений к удаленному рабочему столу и уменьшает свойство **Order** политики авторизации подключений удаленных рабочих столов, за которым следует текущая политика авторизации подключений удаленных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 MoveDown();
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

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

