---
title: Метод Жетпатчпропертиес класса Win32_RDMSVirtualDesktopCollection
description: Извлекает свойства задания подготовки обновлений программного обеспечения для виртуальных машин в коллекции виртуальных рабочих столов.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетпатчпропертиес
- Службы удаленных рабочих столов метода Жетпатчпропертиес, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Жетпатчпропертиес
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969a73e372dee430b280d4d16c267c6d8b75dda236c3ae7362d2392cb1bf8bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099514"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Метод Жетпатчпропертиес \_ класса Win32 рдмсвиртуалдесктопколлектион

Извлекает свойства задания подготовки обновлений программного обеспечения для виртуальных машин в коллекции виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

Время *начала* \[ заполняет\]
</dt> <dd>

Дата и время установки обновлений.

</dd> <dt>

*Форцелогоффтиме* \[ заполняет\]
</dt> <dd>

Дата и время, когда система будет выходить из системы пользователей виртуальных машин.

</dd> <dt>

*Жобгуид* \[ заполняет\]
</dt> <dd>

**Идентификатор GUID** , который однозначно определяет задание подготовки.

</dd> <dt>

*Состояние* \[ заполняет\]
</dt> <dd>

Состояние задания подготовки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Рдмсвиртуалдесктопколлектион Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





