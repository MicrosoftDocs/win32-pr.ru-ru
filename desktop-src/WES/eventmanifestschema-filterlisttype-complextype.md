---
title: Сложный тип Филтерлисттипе
description: Определяет список фильтров, которые контроллер ETW может передать поставщику для дальнейшего ограничения числа записываемых событий.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Журнал событий сложных типов Филтерлисттипе
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341215"
---
# <a name="filterlisttype-complex-type"></a>Сложный тип Филтерлисттипе

Определяет список фильтров, которые контроллер ETW может передать поставщику для дальнейшего ограничения числа записываемых событий.

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент    | Тип                                                             | Описание                   |
|------------|------------------------------------------------------------------|-------------------------------|
| **filter** | [**FilterType**](eventmanifestschema-filtertype-complextype.md) | Список фильтров.<br/> |



## <a name="remarks"></a>Комментарии

Контроллер ETW — это приложение, которое вызывает функцию [**старттраце**](/windows/desktop/ETW/starttrace) для создания сеанса ETW. Дополнительные сведения см. в разделе [Управление сеансами трассировки событий](/windows/desktop/ETW/controlling-event-tracing-sessions). Контроллер может использовать функцию [**тдхенумератепровидерфилтерс**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) для перечисления определенных фильтров. Контроллер может затем передать один или несколько фильтров при вызове функции [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) для включения поставщика. Поставщик получает фильтры вместе с остальными параметрами включения в функции обратного вызова [*енаблекаллбакк*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

