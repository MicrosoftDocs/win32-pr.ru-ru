---
title: Класс Win32_TSGatewayLoadBalancer
description: Описывает набор серверов балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов). Они используются для балансировки нагрузки подключений к шлюзу удаленных рабочих столов на нескольких серверах.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayLoadBalancer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayLoadBalancer, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584077911faf8593e7c26aadd36ca17a0a11d82b18d1d6ade20be1f1444fedf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769874"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>\_Класс Win32 тсгатевайлоадбаланцер

Описывает набор серверов балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов). Они используются для балансировки нагрузки подключений к шлюзу удаленных рабочих столов на нескольких серверах.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсгатевайлоадбаланцер** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсгатевайлоадбаланцер** содержит следующие методы.



| Метод                                                                             | Описание                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**аддсерверс**](addservers-win32-tsgatewayloadbalancer.md)                       | Добавляет серверы в свойство **Servers** .<br/>                                                             |
| [**делетеаллсерверс**](deleteallservers-win32-tsgatewayloadbalancer.md)           | Удаляет все серверы балансировки нагрузки шлюза удаленных рабочих столов, участвующие в ферме балансировки нагрузки.<br/>               |
| [**делетесерверс**](deleteservers-win32-tsgatewayloadbalancer.md)                 | Удаляет серверы из свойства **Servers** .<br/>                                                        |
| [**ислоадбаланЦингсервер**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | Определяет, может ли сервер выполнять балансировку нагрузки.<br/>                                             |
| [**сетсерверс**](setservers-win32-tsgatewayloadbalancer.md)                       | Задает свойство **Servers** с разделенным точкой с запятой списком серверов балансировки нагрузки шлюза удаленных рабочих столов.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсгатевайлоадбаланцер** имеет следующие свойства.

<dl> <dt>

**Серверы**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Разделенный точками с запятой список серверов балансировки нагрузки шлюза удаленных рабочих столов. Это свойство можно изменить с помощью методов [**сетсерверс**](setservers-win32-tsgatewayloadbalancer.md), [**аддсерверс**](addservers-win32-tsgatewayloadbalancer.md), [**делетесерверс**](deleteservers-win32-tsgatewayloadbalancer.md)и [**делетеаллсерверс**](deleteallservers-win32-tsgatewayloadbalancer.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

Для использования этого класса необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_Тсгатевайконнектион Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_Тсгатевайрадиуссервер Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

