---
title: Регистратионинфо. SecurityDescriptor, свойство
description: Для создания скриптов Возвращает или задает дескриптор безопасности задачи.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- планировщик задач свойства SecurityDescriptor
- Планировщик задач свойства SecurityDescriptor, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681746"
---
# <a name="registrationinfosecuritydescriptor-property"></a>Регистратионинфо. SecurityDescriptor, свойство

Для создания скриптов Возвращает или задает дескриптор безопасности задачи. Если во время регистрации задачи был указан другой дескриптор безопасности, он заменит дескриптор безопасности, установленный этим свойством.

## <a name="syntax"></a>Синтаксис


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Значение свойства

Дескриптор безопасности, связанный с задачей.

## <a name="remarks"></a>Комментарии

При чтении или записи XML-кода для задачи дескриптор безопасности задачи указывается с помощью элемента [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





