---
title: Метод Жетстрингпроперти класса Win32_RDSHCollection
description: Извлекает значение свойства строки \_ объекта Win32 рдшколлектион.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстрингпроперти
- Службы удаленных рабочих столов метода Жетстрингпроперти, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Жетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988344"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a>Метод Жетстрингпроперти \_ класса Win32 рдшколлектион

Извлекает значение свойства строки объекта [**Win32 \_ рдшколлектион**](win32-rdshcollection.md) .

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Ключ, определяющий извлекаемое свойство.

</dd> <dt>

*Значение* \[ заполняет\]
</dt> <dd>

Получает полученное значение свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдшколлектион Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





