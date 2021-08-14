---
title: Метод Думпвминфо класса Win32_TSVm
description: Этот член предназначен для внутренних целей тестирования и не должен использоваться в коде.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Думпвминфо
- Службы удаленных рабочих столов метода Думпвминфо, класс Win32_TSVm
- Класс Win32_TSVm службы удаленных рабочих столов, метод Думпвминфо
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c74602e09f7aab4909e78bcd4696a450419e929b89769b35e16f21cbcafc080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354025"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a>Метод Думпвминфо \_ класса Win32 тсвм

Этот член предназначен для внутренних целей тестирования и не должен использоваться в коде.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                             |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                   |
| MOF<br/>                      | <dl> <dt>Тсвмхост. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсвм Win32**](win32-tsvm.md)
</dt> </dl>

 

 





