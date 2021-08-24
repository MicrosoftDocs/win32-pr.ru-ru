---
title: Регистратионинфо. URI, свойство
description: Для создания скриптов Возвращает или задает универсальный код ресурса (URI) задачи.
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- планировщик задач свойства URI
- Планировщик задач свойства URI, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство URI
topic_type:
- apiref
api_name:
- RegistrationInfo.URI
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c34c5dee30115ee430ad072d26e4bd67879988a9f2633cf9da9304e31324b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034084"
---
# <a name="registrationinfouri-property"></a>Регистратионинфо. URI, свойство

Для создания скриптов Возвращает или задает универсальный код ресурса (URI) задачи.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>Значение свойства

Универсальный код ресурса (URI) задачи.

## <a name="remarks"></a>Remarks

При чтении или записи XML для задачи URI задачи указывается с помощью элемента [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





