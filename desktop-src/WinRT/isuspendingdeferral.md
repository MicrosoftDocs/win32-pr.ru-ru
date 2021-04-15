---
description: Управляет отложенной операцией приостановки приложения.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Интерфейс Исуспендингдеферрал (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647170"
---
# <a name="isuspendingdeferral-interface"></a>Интерфейс Исуспендингдеферрал

Управляет отложенной операцией приостановки приложения.

## <a name="members"></a>Элементы

Интерфейс **исуспендингдеферрал** наследует от [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **Исуспендингдеферрал** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **исуспендингдеферрал** содержит следующие методы.



| Метод                                           | Описание                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Завершить**](isuspendingdeferral-complete.md) | Уведомляет систему, что приложение сохранило свои данные и готово к приостановке.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**исуспендинжевентаргс**](isuspendingeventargs.md)
</dt> <dt>

[**исуспендингоператион**](isuspendingoperation.md)
</dt> </dl>

 

 
