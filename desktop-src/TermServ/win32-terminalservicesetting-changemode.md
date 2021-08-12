---
title: Метод Чанжемоде класса Win32_TerminalServiceSetting
description: Метод Чанжемоде задает тип лицензирования текущего сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов).
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Чанжемоде
- Службы удаленных рабочих столов метода Чанжемоде, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Чанжемоде
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2812dd459e13922b1745e55355972092091b4fd9521bc41a46da40769c02021d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604043"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>Метод Чанжемоде \_ класса Win32 терминалсервицесеттинг

Метод **чанжемоде** задает тип лицензирования текущего сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Лиценсингтипе* \[ окне\]
</dt> <dd>

Тип лицензирования, устанавливаемый на основе режима сервера узла сеансов удаленных рабочих столов.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Сервер узла сеансов личных удаленных рабочих столов.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Удаленный рабочий стол для администрирования.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

За устройство/на рабочее место. Допустимо для серверов приложений.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

На пользователя. Допустимо для серверов приложений.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

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

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

