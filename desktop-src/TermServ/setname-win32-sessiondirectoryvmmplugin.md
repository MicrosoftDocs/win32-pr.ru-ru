---
title: Метод SetName класса Win32_SessionDirectoryVMMPlugin
description: Задает имя подключаемого модуля.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetName
- Службы удаленных рабочих столов метода SetName, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод SetName
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6960d08f39e7ce026a36d1644bebf49aec292a44d900974ebd8481379b00dcf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604643"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Метод SetName \_ класса Win32 сессиондиректоривммплугин

Задает имя подключаемого модуля.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*sName* \[ окне\]
</dt> <dd>

Имя подключаемого модуля.

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

 

 





