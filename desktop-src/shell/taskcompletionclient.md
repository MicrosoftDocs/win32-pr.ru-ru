---
description: Включает выполнение задачи.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Интерфейс Тасккомплетионклиент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: d03e52a15e6689b7f1ea98a2f1021874cab6a8967dd148b7eaf685ff3984e8cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773654"
---
# <a name="taskcompletionclient-interface"></a>Интерфейс Тасккомплетионклиент

Включает выполнение задачи.

## <a name="members"></a>Элементы

Интерфейс **тасккомплетионклиент** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Тасккомплетионклиент** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **тасккомплетионклиент** содержит следующие методы.



| Метод                                                                    | Описание                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**апплитасккомплетион**](taskcompletionclient-applytaskcompletion.md)   | Начинает выполнение задачи.<br/> |
| [**ревокетасккомплетион**](taskcompletionclient-revoketaskcompletion.md) | Завершает выполнение задачи.<br/>   |



 

## <a name="remarks"></a>Remarks

Идентификатор GUID для этого интерфейса — "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".

Этот API является устаревшим и может быть недоступен в будущих версиях Windows. Приложения должны использовать API в [**Windows.**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041)Вместо этого используйте пространство имен ApplicationModel. екстендедексекутион.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
