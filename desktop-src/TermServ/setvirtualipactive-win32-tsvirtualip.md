---
title: Метод Сетвиртуалипактиве класса Win32_TSVirtualIP
description: Задает значение свойства Виртуалипактиве.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуалипактиве
- Службы удаленных рабочих столов метода Сетвиртуалипактиве, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Сетвиртуалипактиве
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab43a007a2a8b04e91d5225e648d5667a87c468cbd52c005d85f4ba6496c919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850923"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a>Метод Сетвиртуалипактиве \_ класса Win32 тсвиртуалип

Задает значение свойства **виртуалипактиве** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Виртуалипактиве* \[ окне\]
</dt> <dd>

Тип: **UInt32**

Указывает, активна ли на сервере виртуализация IP-адресов. Это может быть одно из следующих значений.

<dt>

нуль
</dt> <dd>

Виртуализация IP-адресов неактивна.

</dd> <dt>

отличные
</dt> <dd>

Виртуализация IP-адресов активна.

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

 

 





