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
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891741"
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

## <a name="remarks"></a>Комментарии

Разрешения по умолчанию:

-   Учетные записи администратора, системы и удаленный рабочий стол помощника имеют все [разрешения службы удаленных рабочих столов](terminal-services-permissions.md).
-   Учетная запись пользователя удаленный рабочий стол имеет разрешение Вход, подключение, запрос сведений и отправка сообщения.
-   Учетные записи локальной службы и сетевой службы содержат сведения о запросах и разрешение отправлять сообщение.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| Header<br/>                   | <dl> <dt>Netfw. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тспермиссионссеттинг Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

