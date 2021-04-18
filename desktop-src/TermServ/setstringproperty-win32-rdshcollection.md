---
title: Метод Сетстрингпроперти класса Win32_RDSHCollection (Цертенролл. h)
description: Обновляет значение свойства строки \_ объекта Win32 рдшколлектион.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетстрингпроперти
- Службы удаленных рабочих столов метода Сетстрингпроперти, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Сетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2606c195822432138ee67576db54f945c6834cfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672745"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a>Метод Сетстрингпроперти \_ класса Win32 рдшколлектион

Обновляет значение свойства строки объекта [**Win32 \_ рдшколлектион**](win32-rdshcollection.md) .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Ключ, определяющий обновляемое свойство.

</dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

Новое значение свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| Header<br/>                   | <dl> <dt>Цертенролл. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдшколлектион Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





