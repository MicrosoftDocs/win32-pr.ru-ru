---
title: Метод ЕксплиЦитлогон класса Win32_TSLogonSetting
description: Метод ЕксплиЦитлогон задает учетные данные, используемые для проверки подлинности.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ЕксплиЦитлогон
- Службы удаленных рабочих столов метода ЕксплиЦитлогон, класс Win32_TSLogonSetting
- Класс Win32_TSLogonSetting службы удаленных рабочих столов, метод ЕксплиЦитлогон
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7303f06967d26276c7b43e06109cd9b37d664b960946afdffbb4f6a5a7c18821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137787"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Метод ЕксплиЦитлогон \_ класса Win32 тслогонсеттинг

Метод **експлиЦитлогон** задает учетные данные, используемые для проверки подлинности.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя пользователя* \[ окне\]
</dt> <dd>

Учетные данные имени пользователя для входа.

</dd> <dt>

*Домен* \[ окне\]
</dt> <dd>

Учетные данные для входа в домен.

</dd> <dt>

*Пароль* \[ окне\]
</dt> <dd>

Учетные данные для входа на пароль.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное завершение, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_Тслогонсеттинг Win32**](win32-tslogonsetting.md)
</dt> </dl>

 

