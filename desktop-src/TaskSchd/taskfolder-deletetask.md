---
title: Таскфолдер. Делететаск, метод
description: Для создания скриптов удаляет задачу из папки.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- планировщик задач метода Делететаск
- Планировщик задач метода Делететаск, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, метод Делететаск
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802782"
---
# <a name="taskfolderdeletetask-method"></a>Таскфолдер. Делететаск, метод

Для создания скриптов удаляет задачу из папки.

## <a name="syntax"></a>Синтаксис


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* \[ окне\]
</dt> <dd>

Имя задачи, указанной при регистрации задачи. Символ "." нельзя использовать для указания текущей папки задач и ".." символы нельзя использовать для указания родительской папки задач в пути.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Не поддерживается. Значение равно 0

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

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

 

 





