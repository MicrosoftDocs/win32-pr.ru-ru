---
description: Представляет родительский класс, из которого производятся все классы трассировки событий диспетчера объектов.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Класс Обтраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815240"
---
# <a name="obtrace-class"></a>Класс Обтраце

Представляет родительский класс, из которого производятся все классы трассировки событий диспетчера объектов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Участники

Класс **обтраце** не определяет никаких членов.

## <a name="remarks"></a>Примечания

Чтобы включить трассировку событий диспетчера объектов, вызовите функцию [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) с параметром *информатионкласс* , равным значению перечисления [**\_ \_ класса сведений о трассировке**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **трацесистемтрацеенаблефлагсинфо** , а элемент **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) — к **\_ \_ маркеру "PERF OB** " (0x80000040).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |



 

 
