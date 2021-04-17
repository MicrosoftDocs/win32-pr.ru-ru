---
title: Метод Сетвиртуализелупбаккаддрессесенаблед класса Win32_TSVirtualIP
description: Задает значение свойства Виртуализелупбаккаддрессесенаблед.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуализелупбаккаддрессесенаблед
- Службы удаленных рабочих столов метода Сетвиртуализелупбаккаддрессесенаблед, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Сетвиртуализелупбаккаддрессесенаблед
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672535"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>Метод Сетвиртуализелупбаккаддрессесенаблед \_ класса Win32 тсвиртуалип

Задает значение свойства **виртуализелупбаккаддрессесенаблед** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Виртуализелупбаккаддрессесенаблед* \[ окне\]
</dt> <dd>

Указывает, следует ли включить виртуализацию адресов замыкания на себя. Это может быть одно из следующих значений.

<dt>

0
</dt> <dd>

Не включайте петлевой адрес виртуализации.

</dd> <dt>

1
</dt> <dd>

Включить виртуализацию адресов замыкания на себя.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсвиртуалип Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





