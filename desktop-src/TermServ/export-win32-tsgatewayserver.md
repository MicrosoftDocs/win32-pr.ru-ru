---
title: Метод Export класса Win32_TSGatewayServer
description: Возвращает конфигурацию сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) в виде XML-строки.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода экспорта
- Службы удаленных рабочих столов метода экспорта, класс Win32_TSGatewayServer
- Win32_TSGatewayServer службы удаленных рабочих столов класса, метод Export
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989417"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a>Метод Export \_ класса Win32 тсгатевайсервер

Возвращает конфигурацию сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) в виде XML-строки.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ExportType* \[ окне\]
</dt> <dd>

Содержимое для экспорта. Задайте тип экспорта, задав соответствующие биты в параметре *ExportType* . Можно задать несколько типов экспорта. Например, если установлен бит 0, то будут экспортированы службы удаленных рабочих столов политики авторизации подключений (RD CAP). Если заданы значения 0 и 2-го бита, то будут экспортированы политики авторизации подключений к УДАЛЕНным и службы удаленных рабочих столов ресурсам (RD RAP).

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Экспортировать все прописные** (1)


</dt> <dd>

Экспорт всех политик авторизации подключений к удаленным рабочим столам.

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Экспорт всех серверов RADIUS** (2)


</dt> <dd>

Экспорт списка всех серверов политики сети (NPS).

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Экспорт всех политик авторизации** подключений (4)


</dt> <dd>

Экспорт всех политик авторизации подключений к удаленным рабочим столам.

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Экспорт всех RGs** (8)


</dt> <dd>

Экспортируйте все группы ресурсов.

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Экспортировать все серверы LoadBalancing** (16)


</dt> <dd>

Экспортируйте список всех серверов балансировки нагрузки.

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Экспорт всех параметров сервера** (32)


</dt> <dd>

Экспортируйте все параметры сервера, относящиеся к шлюзу удаленных рабочих столов.

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Экспорт всех политик работоспособности** (64)


</dt> <dd>

Экспортируйте все политики работоспособности.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 и Windows Server 2008: * *

Это значение не поддерживается до Windows Server 2016.

</dd> </dl> </dd> <dt>

*Ксмлстринг* \[ заполняет\]
</dt> <dd>

Строка XML-адреса.

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

 

