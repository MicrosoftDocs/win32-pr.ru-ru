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
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266163"
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



 

## <a name="remarks"></a>Примечания

Идентификатор GUID для этого интерфейса — "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".

Этот API является устаревшим и может быть недоступен в будущих версиях Windows. Вместо этого приложения должны использовать API-интерфейсы в пространстве имен [**Windows. ApplicationModel. екстендедексекутион**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
