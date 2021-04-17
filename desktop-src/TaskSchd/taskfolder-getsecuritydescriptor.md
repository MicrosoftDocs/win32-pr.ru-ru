---
title: Таскфолдер. Жетсекуритидескриптор, свойство
description: Для сценариев возвращает дескриптор безопасности для папки.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- планировщик задач свойства Жетсекуритидескриптор
- Планировщик задач свойства Жетсекуритидескриптор, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, свойство Жетсекуритидескриптор
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682011"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>Таскфолдер. Жетсекуритидескриптор, свойство

Для сценариев возвращает дескриптор безопасности для папки.

## <a name="syntax"></a>Синтаксис


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Таскфолдер. Сетсекуритидескриптор**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**Регистередтаск. Сетсекуритидескриптор**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





