---
title: Метод Сетвиртуалипмоде класса Win32_TSVirtualIP
description: Задает значение свойства Виртуалипмоде.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуалипмоде
- Службы удаленных рабочих столов метода Сетвиртуалипмоде, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Сетвиртуалипмоде
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681959"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a>Метод Сетвиртуалипмоде \_ класса Win32 тсвиртуалип

Задает значение свойства **виртуалипмоде** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Виртуалипмоде* \[ окне\]
</dt> <dd>

Тип: **UInt32**

Указывает, какой режим виртуализации IP используется на сервере. Это может быть одно из следующих значений.

<dt>

0
</dt> <dd>

Режим виртуализации IP — для каждого сеанса.

</dd> <dt>

1
</dt> <dd>

Режим виртуализации IP-адресов — "на пользователя".

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсвиртуалип Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





