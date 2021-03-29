---
description: Предоставляет данные для события приостановки приложения.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Интерфейс Исуспендинжевентаргс (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647169"
---
# <a name="isuspendingeventargs-interface"></a>Интерфейс Исуспендинжевентаргс

Предоставляет данные для события приостановки приложения.

## <a name="members"></a>Элементы

Интерфейс **исуспендинжевентаргс** наследует от [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **Исуспендинжевентаргс** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **исуспендинжевентаргс** имеет следующие свойства.



| Свойство                                                                           | Тип доступа           | Описание                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**суспендингоператион**](isuspendingeventargs-suspendingoperation.md)<br/> | Чтение/запись<br/> | Возвращает операцию приостановки приложения.<br/> |



 

## <a name="remarks"></a>Комментарии

Доступ к этому объекту осуществляется при реализации таких обработчиков событий, как [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), и [**Добавление \_ приостановки**](/previous-versions//hh438376(v=vs.85)) для реагирования на события приостановки приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**исуспендингоператион**](isuspendingoperation.md)
</dt> <dt>

[**исуспендингдеферрал**](isuspendingdeferral.md)
</dt> </dl>

 

 
