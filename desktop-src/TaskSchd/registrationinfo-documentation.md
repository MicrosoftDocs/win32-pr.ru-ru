---
title: RegistrationInfo.Doc, свойство ументатион
description: Для создания скриптов Возвращает или задает любую дополнительную документацию для задачи.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- планировщик задач свойств документации
- Свойство документации планировщик задач, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство Documentation
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5832c78fae5c0ee9629077693db7e283369cc8af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135058"
---
# <a name="registrationinfodocumentation-property"></a>RegistrationInfo.Doc, свойство ументатион

Для создания скриптов Возвращает или задает любую дополнительную документацию для задачи.

## <a name="syntax"></a>Синтаксис


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a>Значение свойства

Любая дополнительная документация, связанная с задачей.

## <a name="remarks"></a>Комментарии

При чтении или записи XML для задачи дополнительная документация для задачи указывается с помощью элемента [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) схемы планировщик задач.

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

 

 





