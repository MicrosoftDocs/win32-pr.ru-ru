---
title: Класс Win32_TSGatewayResourceGroup
description: Описывает группу ресурсов, которая сопоставляет набор ресурсов (имен компьютеров) с одной сущностью.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayResourceGroup, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ba4ec4545502d82a3449cee39954deb9b5b2e68bf7c657423e673c582d1c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603892"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>\_Класс Win32 тсгатевайресаурцеграуп

Описывает группу ресурсов, которая сопоставляет набор ресурсов (имен компьютеров) с одной сущностью.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсгатевайресаурцеграуп** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсгатевайресаурцеграуп** содержит следующие методы.



| Метод                                                                  | Описание                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**аддресаурцес**](addresources-win32-tsgatewayresourcegroup.md)       | Добавляет ресурсы в свойство **Resources** для этой группы ресурсов.<br/>      |
| [**Создание**](create-win32-tsgatewayresourcegroup.md)                   | Создает группу ресурсов.<br/>                                                  |
| [**DELETE**](delete-win32-tsgatewayresourcegroup.md)                   | Удаляет эту группу ресурсов.<br/>                                               |
| [**ремовересаурцес**](removeresources-win32-tsgatewayresourcegroup.md) | Удаляет ресурсы из свойства **Resources** для этой группы ресурсов.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Задает свойство **Description** для этой группы ресурсов.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Задает свойство **Name** для этой группы ресурсов.<br/>                        |
| [**сетресаурцес**](setresources-win32-tsgatewayresourcegroup.md)       | Задает свойство **Resources** для этой группы ресурсов.<br/>                   |
| [**Update**](update-win32-tsgatewayresourcegroup.md)                   | Обновляет эту группу ресурсов.<br/>                                               |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсгатевайресаурцеграуп** имеет следующие свойства.

<dl> <dt>

**ассоЦиатедрапс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Разделенный точками с запятой список службы удаленных рабочих столов политик авторизации ресурсов (RD RAP), связанных с этой группой ресурсов.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание группы ресурсов. Это свойство можно изменить с помощью метода [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя группы ресурсов. Это свойство можно изменить с помощью метода [**SetName**](setname-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Ресурсы**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Разделенный точками с запятой список ресурсов в этой группе ресурсов. " \* " Означает все ресурсы. Это свойство можно изменить с помощью методов [**сетресаурцес**](setresources-win32-tsgatewayresourcegroup.md), [**аддресаурцес**](addresources-win32-tsgatewayresourcegroup.md), [**ремовересаурцес**](removeresources-win32-tsgatewayresourcegroup.md)и [**Update**](update-win32-tsgatewayresourcegroup.md) .

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

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

