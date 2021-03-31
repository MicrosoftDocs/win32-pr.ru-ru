---
title: Шовмессажеактион. Title, свойство
description: Для создания скриптов Возвращает или задает заголовок окна сообщения.
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- планировщик задач свойства Title
- Свойство Title планировщик задач, объект Шовмессажеактион
- Планировщик задач объекта Шовмессажеактион, свойство Title
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801601"
---
# <a name="showmessageactiontitle-property"></a>Шовмессажеактион. Title, свойство

\[Этот объект больше не поддерживается. Для отображения сообщения в сеансе пользователя можно использовать Иексекактион с функцией Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .\]

Для создания скриптов Возвращает или задает заголовок окна сообщения.

## <a name="syntax"></a>Синтаксис


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a>Значение свойства

Название окна сообщения.

## <a name="remarks"></a>Комментарии

Параметризованные строки можно использовать в тексте заголовка окна сообщения. Дополнительные сведения см. в разделе "примеры" в [**EventTrigger. валуекуериес**](eventtrigger-valuequeries.md).

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

 

