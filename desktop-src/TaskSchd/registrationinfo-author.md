---
title: Регистратионинфо. Author, свойство
description: Для создания скриптов Возвращает или задает автора задачи.
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- планировщик задач свойства автора
- Свойство Author планировщик задач, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство Author
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7e940ff9da2cfccaa306ebf73080da2a28a091
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071074"
---
# <a name="registrationinfoauthor-property"></a>Регистратионинфо. Author, свойство

Для создания скриптов Возвращает или задает автора задачи.

## <a name="syntax"></a>Синтаксис


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a>Значение свойства

Автор задачи.

## <a name="remarks"></a>Комментарии

При чтении или записи XML-кода для задачи автор задачи указывается с помощью элемента [**Author**](taskschedulerschema-author-registrationinfotype-element.md) схемы планировщик задач.

При задании значения этого свойства значением может быть текст, полученный из файла resource. dll. Для ссылки на текст из файла ресурсов используется специализированная строка. Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса. Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.

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

 

 





