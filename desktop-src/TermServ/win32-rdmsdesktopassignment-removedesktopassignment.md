---
title: Метод Ремоведесктопассигнмент класса Win32_RDMSDesktopAssignment
description: Удаляет назначение рабочего стола.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремоведесктопассигнмент
- Службы удаленных рабочих столов метода Ремоведесктопассигнмент, класс Win32_RDMSDesktopAssignment
- Класс Win32_RDMSDesktopAssignment службы удаленных рабочих столов, метод Ремоведесктопассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682106"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Метод Ремоведесктопассигнмент \_ класса Win32 рдмсдесктопассигнмент

Удаляет назначение рабочего стола

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Коллектионалиас* \[ окне\]
</dt> <dd>

Псевдоним коллекции.

</dd> <dt>

*Десктопнаме* \[ окне\]
</dt> <dd>

Имя рабочего стола.

</dd> <dt>

*Доменпользователя* \[ окне\]
</dt> <dd>

Доменное имя учетной записи пользователя.

</dd> <dt>

*Имя пользователя* \[ окне\]
</dt> <dd>

Имя учетной записи пользователя.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсдесктопассигнмент Win32**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





