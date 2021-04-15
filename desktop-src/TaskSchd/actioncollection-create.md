---
title: ActionCollection. Create, метод
description: Для создания скрипта создает и добавляет в коллекцию новое действие.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- планировщик задач метода Create
- Создание планировщик задач метода, объект ActionCollection
- Планировщик задач объекта ActionCollection, метод Create
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534619"
---
# <a name="actioncollectioncreate-method"></a>ActionCollection. Create, метод

Для создания скрипта создает и добавляет в коллекцию новое действие.

## <a name="syntax"></a>Синтаксис


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тип* \[ окне\]
</dt> <dd>

Для этого параметра задается одна из следующих констант перечисления [**\_ \_ типов действий задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .



| Значение                                                                                                                                                                                                                                                   | Значение                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Задача \_ ДЕЙСТВИЕ \_ exec**</dt> <dt>0</dt> </dl>                          | Действие выполняет операцию командной строки. Например, действие может выполнить сценарий, запустить исполняемый файл или, если указано имя документа, найти связанное с ним приложение и запустить приложение с документом.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Задача \_ \_ \_ Обработчик com действия**</dt> <dt>5</dt> </dl>    | Действие запускает обработчик.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Задача \_ ДЕЙСТВИЕ \_ Отправить \_ электронное письмо**</dt> <dt>6</dt> </dl>       | Это действие отправляет сообщение электронной почты.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Задача \_ ДЕЙСТВИЕ \_ Показывать \_ сообщение**</dt> <dt>7</dt> </dl> | Это действие отображает окно сообщения.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**Action**](action.md) , представляющий новое действие.

## <a name="remarks"></a>Комментарии

К коллекции нельзя добавить более 32 действий.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип действия \_ задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> <dt>

[**Действие**](action.md)
</dt> <dt>

[**ексекактион**](execaction.md)
</dt> <dt>

[**емаилактион**](emailaction.md)
</dt> <dt>

[**шовмессажеактион**](showmessageaction.md)
</dt> <dt>

[**комхандлерактион**](comhandleraction.md)
</dt> </dl>

 

 





