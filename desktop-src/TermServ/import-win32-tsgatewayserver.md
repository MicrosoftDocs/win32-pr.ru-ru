---
title: Метод Import класса Win32_TSGatewayServer
description: Импортирует заданную конфигурацию на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода импорта
- Службы удаленных рабочих столов метода импорта, класс Win32_TSGatewayServer
- Win32_TSGatewayServer службы удаленных рабочих столов класса, метод Import
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988865"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Метод Import \_ класса Win32 тсгатевайсервер

Импортирует заданную конфигурацию на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ImportType* \[ окне\]
</dt> <dd>

Импортируемое содержимое. Задайте тип импорта, задав соответствующие биты в параметре *ImportType* . Можно задать несколько типов импорта. Например, если установлен бит 0, то будут импортированы службы удаленных рабочих столов политики авторизации подключений (RD CAP). Если заданы значения 0 и 2-го бита, то будут импортированы политики авторизации подключений к RD и службы удаленных рабочих столов (RD RAP).

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Импортировать все прописные** (1)


</dt> <dd>

Импорт всех политик авторизации подключений к удаленным рабочим столам.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Импорт всех серверов RADIUS** (2)


</dt> <dd>

Импортируйте список всех серверов сетевых политик (NPS).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Импорт всех политик авторизации** подключений (4)


</dt> <dd>

Импорт всех политик авторизации подключений к удаленным рабочим столам.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Импорт всех RGs** (8)


</dt> <dd>

Импортируйте все группы ресурсов.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Импорт всех серверов LoadBalancing** (16)


</dt> <dd>

Импортируйте список всех серверов балансировки нагрузки.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Импорт всех параметров сервера** (32)


</dt> <dd>

Импортируйте все параметры сервера, относящиеся к шлюзу удаленных рабочих столов.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Импорт всех политик работоспособности** (64)


</dt> <dd>

Импортируйте все политики работоспособности.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 и Windows Server 2008: * *

Это значение не поддерживается до Windows Server 2016.

</dd> </dl> </dd> <dt>

*Ксмлстринг* \[ окне\]
</dt> <dd>

Конфигурация в виде XML-строки.

</dd> <dt>

*Мержеорреплаце* \[ окне\]
</dt> <dd>

Указывает, следует ли объединять или заменять данные при возникновении конфликта.

> [!Note]  
> Слияние еще не реализовано. Поэтому значение этого параметра игнорируется.

 

</dd> <dt>

*Логстринг* \[ заполняет\]
</dt> <dd>

Сведения журнала, формируемые во время операции импорта.

</dd> </dl>

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

[**\_Тсгатевайсервер Win32**](win32-tsgatewayserver.md)
</dt> </dl>

 

