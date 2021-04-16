---
title: Метод Жетжоинеднодекаунт класса Win32_RDMSJoinedNode
description: Возвращает число серверов, на которых установлены указанные роли.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетжоинеднодекаунт
- Службы удаленных рабочих столов метода Жетжоинеднодекаунт, класс Win32_RDMSJoinedNode
- Класс Win32_RDMSJoinedNode службы удаленных рабочих столов, метод Жетжоинеднодекаунт
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672615"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a>Метод Жетжоинеднодекаунт \_ класса Win32 рдмсжоинедноде

Возвращает число серверов, на которых установлены указанные роли.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*roleType* \[ окне\]
</dt> <dd>

Битовое поле, указывающее типы ролей.

<dt>

0
</dt> <dd>

Все

</dd> <dt>

1
</dt> <dd>

Брокер подключение к удаленному рабочему столу (РДКБ)

</dd> <dt>

2
</dt> <dd>

Узел сеансов удаленный рабочий стол (узлов сеансов удаленных рабочих столов)

</dd> <dt>

4
</dt> <dd>

Узел виртуализации удаленных рабочих столов (РДВХ)

</dd> </dl> </dd> <dt>

*Количество* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает число серверов с установленными указанными ролями.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсжоинедноде Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





