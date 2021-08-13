---
title: Метод Кэйвалуекомпареандсет класса Win32_RDSHCollection
description: Сравнивает указанный ключ в коллекции с сравниваемый операнд; Если они совпадают, для ключа задается новое значение. Если ключ не существует, метод вставит ключ в коллекцию.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кэйвалуекомпареандсет
- Службы удаленных рабочих столов метода Кэйвалуекомпареандсет, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Кэйвалуекомпареандсет
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e1aaaf90313c8c1434a65c4ffd1045933ad503245f0dacbf78c2b7e1ca054a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422714"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Метод Кэйвалуекомпареандсет \_ класса Win32 рдшколлектион

Сравнивает указанный ключ в коллекции с сравниваемый операнд; Если они совпадают, для ключа задается новое значение. Если ключ не существует, метод вставит ключ в коллекцию.

## <a name="syntax"></a>Синтаксис


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Сравниваемый ключ.

</dd> <dt>

*NewValue* \[ окне\]
</dt> <dd>

Новое значение.

</dd> <dt>

*Сравниваемый операнд* \[ окне\]
</dt> <dd>

Строка для сравнения ключа.

</dd> <dt>

*Инитиалвалуе* \[ заполняет\]
</dt> <dd>

При успешном или неудачном завершении содержит начальное значение ключа.

</dd> </dl>

## <a name="remarks"></a>Remarks

Обратите внимание, что этот метод может извлекать значение ключа и, как таковой, инкапсулирует функциональность [**кэйвалуежет**](win32-rdshcollection-keyvalueget.md).

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

 

 





