---
title: Регистередтаск. Жетсекуритидескриптор, метод
description: Для создания скриптов возвращает дескриптор безопасности, который используется в качестве учетных данных для зарегистрированной задачи.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- планировщик задач метода Жетсекуритидескриптор
- Планировщик задач метода Жетсекуритидескриптор, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, метод Жетсекуритидескриптор
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989115"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a>Регистередтаск. Жетсекуритидескриптор, метод

Для создания скриптов возвращает дескриптор безопасности, который используется в качестве учетных данных для зарегистрированной задачи.

## <a name="syntax"></a>Синтаксис


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*секуритинформатион* 
</dt> <dd>

Сведения о безопасности из [**\_ сведений о безопасности**](/windows/desktop/SecAuthZ/security-information).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Дескриптор безопасности для зарегистрированной задачи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**регистередтаск**](registeredtask.md)
</dt> <dt>

[**Таскфолдер. Жетсекуритидескриптор**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**Регистередтаск. Сетсекуритидескриптор**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

