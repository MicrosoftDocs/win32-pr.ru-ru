---
title: Метод SetInt32Property класса Win32_RDSHCollection
description: Обновляет значение целочисленного свойства \_ объекта Win32 рдшколлектион.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetInt32Property
- Службы удаленных рабочих столов метода SetInt32Property, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 136bb8ccf34004f747829fb43ee8080ccd1d3132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682070"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a>Метод SetInt32Property \_ класса Win32 рдшколлектион

Обновляет значение целочисленного свойства объекта [**Win32 \_ рдшколлектион**](win32-rdshcollection.md) .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
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
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдшколлектион Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





