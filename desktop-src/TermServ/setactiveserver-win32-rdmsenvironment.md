---
title: Метод Сетактивесервер класса Win32_RDMSEnvironment
description: Задает полное доменное имя среды службы управления удаленный рабочий стол (RDMS) для текущего узла.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетактивесервер
- Службы удаленных рабочих столов метода Сетактивесервер, класс Win32_RDMSEnvironment
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов, метод Сетактивесервер
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490311"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Метод Сетактивесервер \_ класса Win32 рдмсенвиронмент

Задает полное доменное имя среды службы управления удаленный рабочий стол (RDMS) для текущего узла.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

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

[**\_Рдмсенвиронмент Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





