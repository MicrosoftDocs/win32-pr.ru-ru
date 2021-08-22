---
title: Метод Жеттсланаидс класса Win32_TerminalServiceSetting
description: Получает идентификаторы и описания локальных сетевых адаптеров NetBIOS (LANA) и описание службы удаленных рабочих столов сетевых адаптеров.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жеттсланаидс
- Службы удаленных рабочих столов метода Жеттсланаидс, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жеттсланаидс
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c96c840879013f86339cd17136ea97a6c3da9933b1e409cf160779908e4038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059582"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a>Метод Жеттсланаидс \_ класса Win32 терминалсервицесеттинг

Метод **жеттсланаидс** получает идентификаторы и описания локальных сетевых адаптеров NetBIOS (Lana) и описание службы удаленных рабочих столов сетевых адаптеров.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ланаидлист* \[ заполняет\]
</dt> <dd>

Массив номеров LANA.

</dd> <dt>

*Ланаиддескриптионс* \[ заполняет\]
</dt> <dd>

Массив описаний LANA, соответствующий массиву *ланаидлист* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

