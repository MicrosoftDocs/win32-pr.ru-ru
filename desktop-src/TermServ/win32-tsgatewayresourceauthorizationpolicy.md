---
title: Класс Win32_TSGatewayResourceAuthorizationPolicy
description: Описание политики авторизации ресурсов удаленный рабочий стол (RD \ 160; RAP). RD \ 160; Политика авторизации ресурсов позволяет определить, разрешено ли пользователю подключаться к указанному ресурсу через шлюз удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayResourceAuthorizationPolicy, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9748ddc4feccd504d823025ea70877004417717d625c904ccae4445f05e6eb03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999824"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>\_Класс Win32 тсгатевайресаурцеаусоризатионполици

Описание политики авторизации ресурсов (RD RAP) удаленный рабочий стол. Политика авторизации ресурсов удаленных рабочих столов используется для принятия решения о том, разрешено ли пользователю подключаться к указанному ресурсу через шлюз удаленный рабочий стол (шлюз удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсгатевайресаурцеаусоризатионполици** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсгатевайресаурцеаусоризатионполици** содержит следующие методы.



| Метод                                                                                          | Описание                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**аддусерграупнамес**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Добавляет указанные имена групп пользователей в существующие группы пользователей в свойстве **усерграупнамес** .<br/>      |
| [**Создание**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Создает политику авторизации ресурсов удаленных рабочих столов.<br/>                                                                                       |
| [**Удален**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Удаляет текущую политику авторизации ресурсов удаленных рабочих столов.<br/>                                                                              |
| [**ремовеусерграупнамес**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Удаляет указанные имена групп пользователей из существующих групп пользователей в свойстве **усерграупнамес** .<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Задает свойство **Description** для политики авторизации ресурсов удаленных рабочих столов.<br/>                                                        |
| [**сетенаблед**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Включает или отключает политику авторизации ресурсов удаленных рабочих столов, устанавливая свойство **Enabled** .<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Задает свойство **Name** для политики авторизации ресурсов удаленных рабочих столов.<br/>                                                               |
| [**сетпортнумберс**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Задает свойство **портнумберс** для политики авторизации ресурсов удаленных рабочих столов.<br/>                                                        |
| [**сетресаурцеграуп**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Задает свойства **ресаурцеграуптипе** и **ResourceGroupName** .<br/>                                     |
| [**сетусерграупнамес**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Задает свойство **усерграупнамес** для политики авторизации ресурсов удаленных рабочих столов.<br/>                                                     |
| [**Update**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Обновляет текущую политику авторизации ресурсов удаленных рабочих столов.<br/>                                                                              |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсгатевайресаурцеаусоризатионполици** имеет следующие свойства.

<dl> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание политики авторизации ресурсов удаленных рабочих столов. Это свойство изменяется с помощью метода [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Включен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включена ли политика авторизации ресурсов удаленных рабочих столов. Это свойство изменяется с помощью метода [**сетенаблед**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя политики авторизации ресурсов удаленных рабочих столов. Это свойство изменяется с помощью метода [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**портнумберс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список номеров портов, разделенных точкой с запятой, которые разрешены для этой политики. Чтобы разрешить любой номер порта, установите " \* ".

</dd> <dt>

**протоколнамес**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список имен протоколов, разделенных точкой с запятой, которые включены для этой политики. Имена должны соответствовать возвращаемому методу [**жетпротоколнаме**](getprotocolname-win32-tsgatewayserversettings.md) класса [**Win32 \_ тсгатевайсерверсеттингс**](win32-tsgatewayserversettings.md) .

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя группы ресурсов. Это свойство изменяется с помощью метода [**сетресаурцеграуп**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**ресаурцеграуптипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет тип группы ресурсов. Это свойство изменяется с помощью метода [**сетресаурцеграуп**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

<dt>

RG
</dt> <dd>

группа ресурсов;

</dd> <dt>

CG
</dt> <dd>

Группа компьютеров, сохраненная в домен Active Directory Services.

</dd> <dt>

КАЖДОГО
</dt> <dd>

Все ресурсы.

</dd> </dl>

</dd> <dt>

**усерграупнамес**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Разделенный точками с запятой список имен групп пользователей. Если пользователь принадлежит к любой из этих групп пользователей, доступ будет разрешен. Это свойство изменяется с помощью методов [**сетусерграупнамес**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**аддусерграупнамес**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)и [**ремовеусерграупнамес**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .

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

[**\_Тсгатевайлоадбаланцер Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_Тсгатевайрадиуссервер Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

