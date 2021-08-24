---
title: Метод Селектнетворкадаптер класса Win32_TSVirtualIP
description: Задает MAC-адрес сетевого адаптера, используемого для виртуализации IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Селектнетворкадаптер
- Службы удаленных рабочих столов метода Селектнетворкадаптер, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Селектнетворкадаптер
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d27df38f8314720c4ed16d675cdbd06424611d2ccd127a45069586875c82d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865524"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>Метод Селектнетворкадаптер \_ класса Win32 тсвиртуалип

Задает MAC-адрес сетевого адаптера, используемого для виртуализации IP.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нетворкадаптермакаддресс* \[ окне\]
</dt> <dd>

Тип: **строка**

Указывает MAC-адрес сетевого адаптера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

Если MAC-адрес является недопустимым или не существует, или если используется режим виртуализации IP для каждого сеанса, возвращается ошибка.

Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсвиртуалип Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





