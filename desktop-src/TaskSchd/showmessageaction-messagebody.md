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
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891613"
---
# <a name="showmessageactionmessagebody-property"></a>Шовмессажеактион. MessageBody, свойство

\[Этот объект больше не поддерживается. Для отображения сообщения в сеансе пользователя можно использовать Иексекактион с функцией Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .\]

Для создания скриптов Возвращает или задает текст сообщения, отображаемого в тексте окна сообщения.

## <a name="syntax"></a>Синтаксис


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Значение свойства

Текст сообщения, отображаемый в тексте окна сообщения.

## <a name="remarks"></a>Комментарии

Параметризованные строки можно использовать в тексте сообщения в окне сообщения. Дополнительные сведения см. в разделе "примеры" в [**EventTrigger. валуекуериес**](eventtrigger-valuequeries.md).

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

[**шовмессажеактион**](showmessageaction.md)
</dt> </dl>

 

