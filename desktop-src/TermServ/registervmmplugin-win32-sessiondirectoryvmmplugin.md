---
title: Метод Регистервммплугин класса Win32_SessionDirectoryVMMPlugin
description: Регистрирует новый подключаемый модуль VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Регистервммплугин
- Службы удаленных рабочих столов метода Регистервммплугин, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод Регистервммплугин
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415153"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Метод Регистервммплугин \_ класса Win32 сессиондиректоривммплугин

Регистрирует новый подключаемый модуль VMM.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*sName* \[ окне\]
</dt> <dd>

Имя подключаемого модуля.

</dd> <dt>

*спровидер* \[ окне\]
</dt> <dd>

Имя поставщика подключаемого модуля.

</dd> <dt>

*ссервицелокатион* \[ окне\]
</dt> <dd>

Расположение службы, с которой должен связаться подключаемый модуль.

</dd> <dt>

*склассид* \[ окне\]
</dt> <dd>

Идентификатор класса подключаемого модуля.

</dd> <dt>

*Приоритет* \[ окне\]
</dt> <dd>

Приоритет подключаемого модуля. Чем выше значение, тем выше приоритет подключаемого модуля.

</dd> <dt>

*Включено* \[ окне\]
</dt> <dd>

Указывает, включен ли или отключен подключаемый модуль. **Значение true** , если подключаемый модуль включен или **false** в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Сессиондиректоривммплугин Win32**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





