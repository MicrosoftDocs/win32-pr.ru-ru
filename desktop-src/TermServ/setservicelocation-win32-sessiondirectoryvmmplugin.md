---
title: Метод Сетсервицелокатион класса Win32_SessionDirectoryVMMPlugin
description: Задает расположение службы для подключаемого модуля.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсервицелокатион
- Службы удаленных рабочих столов метода Сетсервицелокатион, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод Сетсервицелокатион
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534550"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Метод Сетсервицелокатион \_ класса Win32 сессиондиректоривммплугин

Задает расположение службы для подключаемого модуля.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ссервицелокатион* \[ окне\]
</dt> <dd>

Расположение службы, с которой должен связаться подключаемый модуль.

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

 

 





