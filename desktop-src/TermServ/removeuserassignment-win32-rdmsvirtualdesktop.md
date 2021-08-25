---
title: Метод Ремовеусерассигнмент класса Win32_RDMSVirtualDesktop
description: Удаляет назначение пользователя из виртуального рабочего стола.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовеусерассигнмент
- Службы удаленных рабочих столов метода Ремовеусерассигнмент, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Ремовеусерассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58fa11b22ec089d555fd1e769c71b3fc9d53dbf038ff8b22fb3df559cce59c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988454"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Метод Ремовеусерассигнмент \_ класса Win32 рдмсвиртуалдесктоп

Удаляет назначение пользователя из виртуального рабочего стола.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*VMName* \[ окне\]
</dt> <dd>

Имя виртуальной машины виртуального рабочего стола.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Рдмсвиртуалдесктоп Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





