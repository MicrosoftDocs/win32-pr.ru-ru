---
title: Метод Сетнетворкадаптерланаид класса Win32_TSNetworkAdapterSetting
description: Указывает номер локальной сетевой карты (LANA) для установки сетевого адаптера.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетнетворкадаптерланаид
- Службы удаленных рабочих столов метода Сетнетворкадаптерланаид, класс Win32_TSNetworkAdapterSetting
- Класс Win32_TSNetworkAdapterSetting службы удаленных рабочих столов, метод Сетнетворкадаптерланаид
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803772"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Метод Сетнетворкадаптерланаид \_ класса Win32 тснетворкадаптерсеттинг

Метод **сетнетворкадаптерланаид** указывает номер локальной сети (Lana) сетевого адаптера, который нужно установить. Если указанный идентификатор LANA недопустим или не существует, возвращается ошибка. Список доступных идентификаторов LANA можно получить, перечисляя свойство **девицеидлист** в классе [**Win32 \_ тснетворкадаптерсеттинг**](win32-tsnetworkadaptersetting.md) .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нетворкадаптерланаид* \[ окне\]
</dt> <dd>

Номер LANA устанавливаемого сетевого адаптера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тснетворкадаптерсеттинг Win32**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

