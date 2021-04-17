---
title: Метод Енумаусентикатионплугинс класса Win32_TSGatewayServerSettings
description: Перечисляет все зарегистрированные подключаемые модули проверки подлинности.
ms.assetid: a5c1859d-e20c-4c72-aef5-ef9941edf73e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енумаусентикатионплугинс
- Службы удаленных рабочих столов метода Енумаусентикатионплугинс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енумаусентикатионплугинс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthenticationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0cd9d059a79749f657c6191e68e7bcd08555cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672550"
---
# <a name="enumauthenticationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Енумаусентикатионплугинс \_ класса Win32 тсгатевайсерверсеттингс

Перечисляет все зарегистрированные подключаемые модули проверки подлинности.

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnumAuthenticationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Плугиннамес* \[ заполняет\]
</dt> <dd>

Тип: **строка \[ \]**

Массив **строк** , который получает имена зарегистрированных подключаемых модулей проверки подлинности.

</dd> <dt>

*Идентификаторы CLSID* \[ заполняет\]
</dt> <dd>

Тип: **строка \[ \]**

Массив **строк** , который получает идентификаторы CLSID зарегистрированных подключаемых модулей проверки подлинности.

</dd> <dt>

*Описание* \[ заполняет\]
</dt> <dd>

Тип: **строка \[ \]**

Массив **строк** , который получает описания зарегистрированных подключаемых модулей проверки подлинности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

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

 

