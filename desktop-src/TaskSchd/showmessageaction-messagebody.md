---
title: Шовмессажеактион. MessageBody, свойство
description: Для создания скриптов Возвращает или задает текст сообщения, отображаемого в тексте окна сообщения.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- планировщик задач свойства MessageBody
- Планировщик задач свойства MessageBody, объект Шовмессажеактион
- Планировщик задач объекта Шовмессажеактион, свойство MessageBody
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5b408ad8642cc17b85d783a8f26d7de3322a26309897e4d9b3c128401449d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139347"
---
# <a name="showmessageactionmessagebody-property"></a>Шовмессажеактион. MessageBody, свойство

\[Этот объект больше не поддерживается. для отображения сообщения в сеансе пользователя можно использовать иексекактион с функцией Windows scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .\]

Для создания скриптов Возвращает или задает текст сообщения, отображаемого в тексте окна сообщения.

## <a name="syntax"></a>Синтаксис


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Значение свойства

Текст сообщения, отображаемый в тексте окна сообщения.

## <a name="remarks"></a>Remarks

Параметризованные строки можно использовать в тексте сообщения в окне сообщения. Дополнительные сведения см. в разделе "примеры" в [**EventTrigger. валуекуериес**](eventtrigger-valuequeries.md).

При задании значения этого свойства значением может быть текст, полученный из файла .dll ресурсов. Для ссылки на текст из файла ресурсов используется специализированная строка. Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ Dll — это \] путь к .dll файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса. Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                    |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                                                       |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**шовмессажеактион**](showmessageaction.md)
</dt> </dl>

 

