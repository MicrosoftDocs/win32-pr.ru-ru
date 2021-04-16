---
title: Метод Сетсервервеигхт класса Win32_TSSessionDirectory
description: Задает значение веса сервера для балансировки нагрузки подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсервервеигхт
- Службы удаленных рабочих столов метода Сетсервервеигхт, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сетсервервеигхт
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491607"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Метод Сетсервервеигхт \_ класса Win32 тссессиондиректори

Задает значение веса сервера для балансировки нагрузки подключение к удаленному рабочему столу Broker (RDCB).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сервервеигхтвалуе* \[ окне\]
</dt> <dd>

Тип: **UInt32**

Значение веса сервера. Допустимый диапазон — от 1 до 10000.

</dd> </dl>

## <a name="remarks"></a>Комментарии

По умолчанию в пользовательском интерфейсе службы удаленных рабочих столов конфигурации значение веса сервера равно 100. Вес сервера является относительным. Таким образом, если присвоить одному серверу значение 100 и одно значение 200, то сервер с относительным весом, равным 200, получит удвоенное число сеансов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тссессиондиректори Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

