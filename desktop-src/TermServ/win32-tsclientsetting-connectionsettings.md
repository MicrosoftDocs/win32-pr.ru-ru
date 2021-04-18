---
title: Метод ConnectionSettings класса Win32_TSClientSetting
description: Метод ConnectionSettings задает параметры сеанса, которые применяются к процессу подключения и входа.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ConnectionSettings
- Службы удаленных рабочих столов метода ConnectionSettings, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534061"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Метод ConnectionSettings \_ класса Win32 тсклиентсеттинг

Метод **ConnectionSettings** задает параметры сеанса, которые применяются к процессу подключения и входа.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Коннектклиентдривесатлогон* \[ окне\]
</dt> <dd>

Флаг включения или отключения свойства **коннектклиентдривесатлогон** , которое указывает, будут ли диски клиента автоматически подключены во время процедуры входа в систему.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Диски клиента не подключаются автоматически.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Диски клиента автоматически соединяются.

</dd> </dl> </dd> <dt>

*Коннектпринтератлогон* \[ окне\]
</dt> <dd>

Флаг включения или отключения свойства **коннектпринтератлогон** , которое указывает, будут ли все сопоставленные локальные клиентские принтеры автоматически подключены во время процедуры входа в систему.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Все сопоставленные локальные принтеры не подключены автоматически.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Все сопоставленные локальные принтеры автоматически соединяются.

</dd> </dl> </dd> <dt>

*Дефаулттоклиентпринтер* \[ окне\]
</dt> <dd>

Флаг включения или отключения свойства **дефаулттоклиентпринтер** , которое указывает, будут ли задания печати автоматически отправляться на локальный принтер клиента.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Задания печати не отправляются автоматически.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Задания печати автоматически отправляются.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметры соединения пользователя переопределяются сервером.

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсклиентсеттинг Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

