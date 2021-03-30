---
title: Метод method класса Win32_TSGetIcon
description: Возвращает содержимое указанного значка.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Метод службы удаленных рабочих столов
- Метод службы удаленных рабочих столов, Win32_TSGetIcon класс
- Класс Win32_TSGetIcon службы удаленных рабочих столов, метод "Icon"
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988282"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>Метод method \_ класса Win32 тсжетикон

Возвращает содержимое указанного значка.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь к файлу* \[ окне\]
</dt> <dd>

Указывает путь к файлу, содержащему значок

</dd> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Задает индекс значка в файле.

</dd> <dt>

*Иконконтентс* \[ заполняет\]
</dt> <dd>

При успешном завершении содержит содержимое значка.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тсаллов. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсжетикон Win32**](win32-tsgeticon.md)
</dt> </dl>

 

 





