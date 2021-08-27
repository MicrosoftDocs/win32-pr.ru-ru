---
title: Метод Селектнетворкадаптерип класса Win32_TSNetworkAdapterSetting
description: Выбирает сетевой адаптер на основе IP-адреса адаптера.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Селектнетворкадаптерип
- Службы удаленных рабочих столов метода Селектнетворкадаптерип, класс Win32_TSNetworkAdapterSetting
- Класс Win32_TSNetworkAdapterSetting службы удаленных рабочих столов, метод Селектнетворкадаптерип
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a88c4820e4537d9c0fb1833b67eb2660a7fb5618189023dfe2217f222efa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008374"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Метод Селектнетворкадаптерип \_ класса Win32 тснетворкадаптерсеттинг

Выбирает сетевой адаптер на основе IP-адреса адаптера.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нетворкадаптерип* \[ окне\]
</dt> <dd>

IP-адрес устанавливаемого сетевого адаптера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль, если указанный IP-адрес является допустимым, и возвращает код ошибки WMI, если IP-адрес является недопустимым или не существует. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Remarks

IP-адрес сетевого адаптера можно получить, перечисляя свойства класса [**Win32 \_ тснетворкадаптерлистсеттинг**](win32-tsnetworkadapterlistsetting.md) .

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тснетворкадаптерсеттинг Win32**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

