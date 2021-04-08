---
title: Метод Сетдефаултплугинсандрециклерпкаппликатионпулс класса Win32_TSGatewayServerSettings
description: Задает текущие подключаемые модули проверки подлинности и авторизации для сервера шлюза удаленный рабочий стол (шлюзов удаленных рабочих столов) и перезапускает пулы приложений RPC в службах IIS.
ms.assetid: 1eac9e42-e533-4020-b2b6-571063f18c3c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетдефаултплугинсандрециклерпкаппликатионпулс
- Службы удаленных рабочих столов метода Сетдефаултплугинсандрециклерпкаппликатионпулс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетдефаултплугинсандрециклерпкаппликатионпулс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetDefaultPluginsAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ead29e987b68ec3f041010be5dde64d8a2b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989244"
---
# <a name="setdefaultpluginsandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Сетдефаултплугинсандрециклерпкаппликатионпулс \_ класса Win32 тсгатевайсерверсеттингс

Задает текущие подключаемые модули проверки подлинности и авторизации для сервера шлюза удаленный рабочий стол (шлюзов удаленных рабочих столов) и перезапускает пулы приложений RPC в службах IIS.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetDefaultPluginsAndRecycleRpcApplicationPools();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Вызов этого метода приводит к отключению всех существующих подключений.

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

