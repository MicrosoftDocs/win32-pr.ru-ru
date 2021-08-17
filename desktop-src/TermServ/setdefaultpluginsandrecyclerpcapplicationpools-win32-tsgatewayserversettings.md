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
ms.openlocfilehash: 61272f6abe62b719667668d60ecdb7ae97c5da717893acd3b89413012c7612d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137997"
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

## <a name="remarks"></a>Remarks

Вызов этого метода приводит к отключению всех существующих подключений.

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

