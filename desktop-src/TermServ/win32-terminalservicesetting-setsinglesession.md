---
title: Метод Сетсинглесессион класса Win32_TerminalServiceSetting
description: Метод Сетсинглесессион задает свойство Синглесессион для класса.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсинглесессион
- Службы удаленных рабочих столов метода Сетсинглесессион, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетсинглесессион
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682065"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a>Метод Сетсинглесессион \_ класса Win32 терминалсервицесеттинг

Метод **сетсинглесессион** задает свойство **синглесессион** для класса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Синглесессион* \[ окне\]
</dt> <dd>

Флаг отключения или включения свойства **синглесессион** , которое определяет, ограничен ли пользователь одним или несколькими сеансами службы удаленных рабочих столов.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Отключите свойство.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Включите свойство.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное завершение, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

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

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

