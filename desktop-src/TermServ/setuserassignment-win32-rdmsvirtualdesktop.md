---
title: Метод Сетусерассигнмент класса Win32_RDMSVirtualDesktop
description: Назначает пользователю виртуальный рабочий стол.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетусерассигнмент
- Службы удаленных рабочих столов метода Сетусерассигнмент, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Сетусерассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38f87209ba8c8ebd82637f72cea2e798844e6081cd000f2161ee21681422e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349415"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Метод Сетусерассигнмент \_ класса Win32 рдмсвиртуалдесктоп

Назначает пользователю виртуальный рабочий стол.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя пользователя* \[ окне\]
</dt> <dd>

Имя пользователя.

</dd> <dt>

*Доменпользователя* \[ окне\]
</dt> <dd>

Доменное имя пользователя.

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

[**\_Рдмсвиртуалдесктоп Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





