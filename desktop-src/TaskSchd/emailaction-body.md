---
title: Емаилактион. Body, свойство
description: Для сценариев Возвращает или задает текст сообщения электронной почты, содержащего сообщение электронной почты.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Свойство Body планировщик задач
- Свойство Body планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57daf8d16da9f77a88d91a23cfaea88d1c3e27adb09a0d502b447b5987fce2ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100384"
---
# <a name="emailactionbody-property"></a>Емаилактион. Body, свойство

\[Этот объект больше не поддерживается. Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]

Для сценариев Возвращает или задает текст сообщения электронной почты, содержащего сообщение электронной почты.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
EmailAction.Body As String
```



## <a name="property-value"></a>Значение свойства

Текст сообщения электронной почты, содержащего сообщение.

## <a name="remarks"></a>Remarks

При задании значения этого свойства значением может быть текст, полученный из файла .dll ресурсов. Для ссылки на текст из файла ресурсов используется специализированная строка. Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ Dll — это \] путь к .dll файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса. Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                    |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                                                       |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**емаилактион**](emailaction.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

