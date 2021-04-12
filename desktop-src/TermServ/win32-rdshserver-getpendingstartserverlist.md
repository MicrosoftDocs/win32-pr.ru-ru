---
title: Метод Жетпендингстартсерверлист класса Win32_RDSHServer
description: Возвращает список серверов, ожидающих запуска.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетпендингстартсерверлист
- Службы удаленных рабочих столов метода Жетпендингстартсерверлист, класс Win32_RDSHServer
- Класс Win32_RDSHServer службы удаленных рабочих столов, метод Жетпендингстартсерверлист
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415632"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Метод Жетпендингстартсерверлист \_ класса Win32 рдшсервер

Возвращает список серверов, ожидающих запуска.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*макссерверс* \[ окне\]
</dt> <dd>

Максимальное число серверов, возвращаемых в списке.

</dd> <dt>

*Серверфкднс* \[ заполняет\]
</dt> <dd>

При успешном выполнении содержит коллекцию полных доменных имен серверов, ожидающих запуска.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Список серверов сбрасывается после каждого вызова, чтобы следующий вызов не получит дублирующий сервер.

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

[**\_Рдшсервер Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





