---
title: Регистратионинфо. Description, свойство
description: Для создания скриптов Возвращает или задает описание задачи.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- планировщик задач Свойства описания
- Свойство Description планировщик задач, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство Description
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6f141eddc40b21f1cf49e490fe30df5844e6029f821d9811b0e62ea55fa8ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872464"
---
# <a name="registrationinfodescription-property"></a>Регистратионинфо. Description, свойство

Для создания скриптов Возвращает или задает описание задачи.

## <a name="syntax"></a>Синтаксис


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a>Значение свойства

Описание задачи.

## <a name="remarks"></a>Remarks

При чтении или записи XML для задачи описание задачи указывается с помощью элемента [**Description**](taskschedulerschema-description-registrationinfotype-element.md) схемы планировщик задач.

При задании значения этого свойства значением может быть текст, полученный из файла .dll ресурсов. Для ссылки на текст из файла ресурсов используется специализированная строка. Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ Dll — это \] путь к .dll файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса. Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Требования



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

 

 





