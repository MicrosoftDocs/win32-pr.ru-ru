---
title: Метод Кэйвалуежет класса Win32_RDSHCollection
description: Извлекает значение, связанное с указанным ключом в коллекции.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кэйвалуежет
- Службы удаленных рабочих столов метода Кэйвалуежет, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Кэйвалуежет
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 943db8db044758e7f78e7d79b4ae5280c6ce51281b5858237a24e5f83add33a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422684"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a>Метод Кэйвалуежет \_ класса Win32 рдшколлектион

Извлекает значение, связанное с указанным ключом в коллекции.

## <a name="syntax"></a>Синтаксис


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Ключ, определяющий значение, которое вы хотите получить.

</dd> <dt>

*Значение* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает значение, связанное с указанным ключом.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдшколлектион Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





