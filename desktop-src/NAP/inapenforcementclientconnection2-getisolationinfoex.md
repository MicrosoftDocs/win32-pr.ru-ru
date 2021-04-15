---
title: Метод INapEnforcementClientConnection2 Жетисолатионинфоекс (Напенфорцементклиент. h)
description: Используется для получения сведений о изоляции клиента.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Метод Жетисолатионинфоекс NAP
- Метод Жетисолатионинфоекс NAP, интерфейс INapEnforcementClientConnection2
- INapEnforcementClientConnection2 интерфейса NAP, метод Жетисолатионинфоекс
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493239"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a>Метод INapEnforcementClientConnection2:: Жетисолатионинфоекс

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **INapEnforcementClientConnection2:: жетисолатионинфоекс** используется для получения сведений о изоляции клиента.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*исолатионинфо* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , которая содержит подключение и расширенные сведения о состоянии клиента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                     | Описание                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>           | Операция успешно завершена.<br/>                                    |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl> | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>  | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |



 

## <a name="remarks"></a>Комментарии

Эта информация задается Напажент после обработки [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) и не может быть задана в принудительном применении.

SHA должен освободить структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , вызвав [**фриисолатионинфоекс**](freeisolationinfoex.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Напенфорцементклиент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напенфорцементклиент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





