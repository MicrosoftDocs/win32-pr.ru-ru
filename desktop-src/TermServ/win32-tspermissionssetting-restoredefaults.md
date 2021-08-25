---
title: Метод Ресторедефаултс класса Win32_TSPermissionsSetting (Netfw. h)
description: Восстанавливает значения набора разрешений по умолчанию для терминала.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ресторедефаултс
- Службы удаленных рабочих столов метода Ресторедефаултс, класс Win32_TSPermissionsSetting
- Класс Win32_TSPermissionsSetting службы удаленных рабочих столов, метод Ресторедефаултс
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef81f4b3008f68129026a90d1b2e98e8c13c298537952175e116c9c8e02c4f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769454"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Метод Ресторедефаултс \_ класса Win32 тспермиссионссеттинг

Метод **ресторедефаултс** восстанавливает значения набора разрешений по умолчанию для терминала.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное выполнение, в противном случае — сбой.

## <a name="remarks"></a>Remarks

Разрешения по умолчанию:

-   Учетные записи администратора, системы и удаленный рабочий стол помощника имеют все [разрешения службы удаленных рабочих столов](terminal-services-permissions.md).
-   учетная запись пользователя удаленный рабочий стол имеет разрешение вход, Подключение, сведения о запросе и отправка сообщения.
-   Учетные записи локальной службы и сетевой службы содержат сведения о запросах и разрешение отправлять сообщение.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Netfw. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тспермиссионссеттинг Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

