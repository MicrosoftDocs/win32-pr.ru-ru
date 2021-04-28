---
title: Метод СетдисаблефорЦиблелогофф класса Win32_TerminalServiceSetting
description: Метод СетдисаблефорЦиблелогофф класса Win32_TerminalServiceSetting. Этот метод не поддерживается.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода СетдисаблефорЦиблелогофф
- Службы удаленных рабочих столов метода СетдисаблефорЦиблелогофф, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод СетдисаблефорЦиблелогофф
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103712"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a>Метод СетдисаблефорЦиблелогофф \_ класса Win32 терминалсервицесеттинг

Этот метод не поддерживается.

**Windows Vista и Windows Server 2008:** Включает или отключает возможность принудительного завершения работы администратора, вошедшего в консоль.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ДисаблефорЦиблелогофф* \[ окне\]
</dt> <dd>

Флаг отключения или включения свойства **дисаблефорЦиблелогофф** , которое определяет, можно ли принудительно завершить работу администратора, выполнившего вход в консоль.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Отключите свойство. Подключенный администратор может принудительно завершить работу.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Включите свойство. Не удается принудительно завершить работу подключенного администратора.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное завершение; в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Окончание поддержки клиента<br/>    | Windows Vista<br/>                                                                |
| Поддержка конца сервера<br/>    | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





