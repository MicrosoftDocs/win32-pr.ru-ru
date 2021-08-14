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
ms.openlocfilehash: c12b3ca9d66817972d75bd3ffbab61bcdcdff5dcc227e680ed6548f77d1b0de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402404"
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

 

 





