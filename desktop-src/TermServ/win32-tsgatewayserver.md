---
title: Класс Win32_TSGatewayServer
description: Используется для конкретных операций сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayServer, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cd6c24447e7ba3bc22788484b2ac9e437ee947243c17a676728d2a336bd326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603894"
---
# <a name="win32_tsgatewayserver-class"></a>\_Класс Win32 тсгатевайсервер

Используется для конкретных операций сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсгатевайсервер** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсгатевайсервер** содержит следующие методы.



| Метод                                                                                   | Описание                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**креатеселфсигнедцертификате**](createselfsignedcertificate-win32-tsgatewayserver.md) | Создает самозаверяющий сертификат с указанным именем субъекта и возвращает хэш сертификата как параметр "out".<br/> |
| [**Экспорт**](export-win32-tsgatewayserver.md)                                           | Возвращает конфигурацию сервера шлюза удаленных рабочих столов в виде XML-строки.<br/>                                                       |
| [**Импорт**](import-win32-tsgatewayserver.md)                                           | Импортирует заданную конфигурацию на сервер шлюза удаленных рабочих столов.<br/>                                                             |



 

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

