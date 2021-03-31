---
title: Таскфолдер. Сетсекуритидескриптор, свойство
description: Для сценариев задает дескриптор безопасности для папки.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- планировщик задач свойства Сетсекуритидескриптор
- Планировщик задач свойства Сетсекуритидескриптор, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, свойство Сетсекуритидескриптор
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988422"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>Таскфолдер. Сетсекуритидескриптор, свойство

Для сценариев задает дескриптор безопасности для папки.

## <a name="syntax"></a>Синтаксис


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Список управления доступом (ACL) можно указать в дескрипторе безопасности для папки задач, чтобы разрешить или запретить определенным пользователям и группам доступ к папке задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Регистередтаск. Сетсекуритидескриптор**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**Таскфолдер. Жетсекуритидескриптор**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





