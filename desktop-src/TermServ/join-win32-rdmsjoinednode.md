---
title: Метод join класса Win32_RDMSJoinedNode
description: Добавляет узел в службы удаленный рабочий стол Management Services (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Join
- Метод Join службы удаленных рабочих столов, класс Win32_RDMSJoinedNode
- Класс Win32_RDMSJoinedNode службы удаленных рабочих столов, метод Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415029"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Метод Join \_ класса Рдмсжоинедноде Win32

Добавляет узел в службы удаленный рабочий стол Management Services (RDMS).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нодефкдн* \[ окне\]
</dt> <dd>

Полное доменное имя узла.

</dd> <dt>

*Нодесид* \[ окне\]
</dt> <dd>

Идентификатор безопасности (SID) узла.

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

[**\_Рдмсжоинедноде Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





