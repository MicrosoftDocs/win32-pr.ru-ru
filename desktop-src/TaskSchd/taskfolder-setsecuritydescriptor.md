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
ms.openlocfilehash: 8416e14a5415de86f8ad3f4a1181ce231ecfbdc875e36e9e3fd14014de8c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033794"
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

## <a name="remarks"></a>Remarks

Список управления доступом (ACL) можно указать в дескрипторе безопасности для папки задач, чтобы разрешить или запретить определенным пользователям и группам доступ к папке задач.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Регистередтаск. Сетсекуритидескриптор**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**Таскфолдер. Жетсекуритидескриптор**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





