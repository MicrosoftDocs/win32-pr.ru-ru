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
ms.openlocfilehash: 8cf30fe0c7b028c819477bcf0c66c2b674fc588286916be1cd1fd1a6b207770d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328754"
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

## <a name="members"></a>Члены

Класс **обтраце** не определяет никаких членов.

## <a name="remarks"></a>Remarks

Чтобы включить трассировку событий диспетчера объектов, вызовите функцию [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) с параметром *информатионкласс* , равным значению перечисления [**\_ \_ класса сведений о трассировке**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **трацесистемтрацеенаблефлагсинфо** , а элемент **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) — к **\_ \_ маркеру "PERF OB** " (0x80000040).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |



 

 
