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
ms.openlocfilehash: c5c3aa83bc05952007d9114ad9812068de5b5b0bd82a4ce9e14e4d5ba1025bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759565"
---
# <a name="registrationinfosecuritydescriptor-property"></a>Регистратионинфо. SecurityDescriptor, свойство

Для создания скриптов Возвращает или задает дескриптор безопасности задачи. Если во время регистрации задачи был указан другой дескриптор безопасности, он заменит дескриптор безопасности, установленный этим свойством.

## <a name="syntax"></a>Синтаксис


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Значение свойства

Дескриптор безопасности, связанный с задачей.

## <a name="remarks"></a>Remarks

При чтении или записи XML-кода для задачи дескриптор безопасности задачи указывается с помощью элемента [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





