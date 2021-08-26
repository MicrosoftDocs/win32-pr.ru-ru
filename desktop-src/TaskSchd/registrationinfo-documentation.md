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
ms.openlocfilehash: 31878417d6a225c5fa7c67569d557a4c6d7a716a24bffd94dfe58a84e3809a37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100184"
---
# <a name="registrationinfodocumentation-property"></a>RegistrationInfo.Doc, свойство ументатион

Для создания скриптов Возвращает или задает любую дополнительную документацию для задачи.

## <a name="syntax"></a>Синтаксис


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a>Значение свойства

Любая дополнительная документация, связанная с задачей.

## <a name="remarks"></a>Remarks

При чтении или записи XML для задачи дополнительная документация для задачи указывается с помощью элемента [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) схемы планировщик задач.

При задании значения этого свойства значением может быть текст, полученный из файла .dll ресурсов. Для ссылки на текст из файла ресурсов используется специализированная строка. Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ Dll — это \] путь к .dll файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса. Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





