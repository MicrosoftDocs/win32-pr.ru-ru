---
description: Удаляет объект Иконтекстлинк из коллекции ссылок объекта Иконтекстноде.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: 'Иконтекстноде: метод:D Елетеконтекстлинк (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 39a36ed8a74accdc7da3eed4c98a96d9ee6abbaa4f52b5c71c367250321d28b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044845"
---
# <a name="icontextnodedeletecontextlink-method"></a>Иконтекстноде: метод:D Елетеконтекстлинк

Удаляет объект [**иконтекстлинк**](icontextlink.md) из коллекции ссылок объекта [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекстлинктоделете* \[ окне\]
</dt> <dd>

Удаляемый объект [**иконтекстлинк**](icontextlink.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Ссылка на контекст имеет исходный узел и узел назначения (см. раздел [**иконтекстлинк:: жетсаурценоде**](icontextlink-getsourcenode.md) and [**Иконтекстлинк:: жетдестинатионноде**](icontextlink-getdestinationnode.md)). Этот метод удаляет [**иконтекстлинк**](icontextlink.md) из коллекции ссылок на исходный и конечный узлы (см. раздел [**Иконтекстноде:: жетконтекстлинкс**](icontextnode-getcontextlinks.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**иконтекстлинк**](icontextlink.md)
</dt> <dt>

[**Иконтекстноде:: Аддконтекстлинк**](icontextnode-addcontextlink.md)
</dt> <dt>

[**Иконтекстноде:: Жетконтекстлинкс**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




