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
ms.openlocfilehash: 61bb46512414c7057d7ec9db5ff4b6fab859f8bb9e6aec5c537250b0baa24e9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422654"
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

## <a name="remarks"></a>Remarks

Список серверов сбрасывается после каждого вызова, чтобы следующий вызов не получит дублирующий сервер.

## <a name="requirements"></a>Requirements (Требования)



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

 

 





