---
title: Метод Сетаусентикатионплугин класса Win32_TSGatewayServerSettings
description: Задает текущий подключаемый модуль аутентификации для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: b79a5e7c-bf55-48f6-a6c0-5338e7eee2a1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетаусентикатионплугин
- Службы удаленных рабочих столов метода Сетаусентикатионплугин, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетаусентикатионплугин
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be1da91b281e8a47c2663fe09f6b7f172dca8d4d246f0fe708139fe859955a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058552"
---
# <a name="setauthenticationplugin-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Сетаусентикатионплугин \_ класса Win32 тсгатевайсерверсеттингс

Задает текущий подключаемый модуль аутентификации для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetAuthenticationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PluginName* \[ окне\]
</dt> <dd>

Тип: **строка**

Имя нового подключаемого модуля текущей проверки подлинности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Чтобы обеспечить работу подключаемого модуля проверки подлинности, необходимо вызвать метод [**рециклерпкаппликатионпулс**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) .

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**рециклерпкаппликатионпулс**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

