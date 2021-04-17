---
title: Емаилактион. subject, свойство
description: Для создания скриптов Возвращает или задает тему сообщения электронной почты.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Свойство Subject планировщик задач
- Свойство Subject планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673121"
---
# <a name="emailactionsubject-property"></a>Емаилактион. subject, свойство

\[Этот объект больше не поддерживается. Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) в качестве обходного пути.\]

Для создания скриптов Возвращает или задает тему сообщения электронной почты.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a>Значение свойства

Тема сообщения электронной почты.

## <a name="remarks"></a>Комментарии

При задании значения этого свойства значением может быть текст, полученный из файла resource. dll. Для ссылки на текст из файла ресурсов используется специализированная строка. Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса. Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                    |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                                                       |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**емаилактион**](emailaction.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

