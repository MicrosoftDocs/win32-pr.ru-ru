---
title: Метод Сеталловдвм класса Win32_TSClientSetting
description: Задает свойство Алловдвм.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеталловдвм
- Службы удаленных рабочих столов метода Сеталловдвм, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сеталловдвм
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672637"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a>Метод Сеталловдвм \_ класса Win32 тсклиентсеттинг

Задает свойство **алловдвм** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Алловдвм* \[ окне\]
</dt> <dd>

Новое значение свойства **алловдвм** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметры соединения пользователя переопределяются сервером.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>                                                               |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсклиентсеттинг Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

 





