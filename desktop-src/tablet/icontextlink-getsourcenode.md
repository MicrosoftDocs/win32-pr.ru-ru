---
description: Извлекает объект Иконтекстноде, являющийся источником для этого Иконтекстлинк.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'Метод Иконтекстлинк:: Жетсаурценоде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 609f3012608586f7e6c3279cd0dab4232f58ca3e0e31145124622e87684e06f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940414"
---
# <a name="icontextlinkgetsourcenode-method"></a>Метод Иконтекстлинк:: Жетсаурценоде

Извлекает объект [**иконтекстноде**](icontextnode.md) , являющийся источником для этого [**иконтекстлинк**](icontextlink.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппсркконтекстнодеид* \[ заполняет\]
</dt> <dd>

Указатель на объект [**иконтекстноде**](icontextnode.md) , являющийся источником для этого [**иконтекстлинк**](icontextlink.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппсркконтекстнодеид* , когда больше не нужно использовать исходный узел.

 

Если объект [**иконтекстлинк**](icontextlink.md) связан между узлом, который содержит запись, и узлом, содержащим рисование, то исходный узел обычно является узлом, содержащим рисование.

Если объект [**иконтекстлинк**](icontextlink.md) имеет тип ссылки, включающий (см. [**Иконтекстлинк:: жетконтекстлинкдиректион**](icontextlink-getcontextlinkdirection.md)), то исходный узел является узлом, который заключает в себя узел назначения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстлинк**](icontextlink.md)
</dt> <dt>

[**Иконтекстлинк:: Жетдестинатионноде**](icontextlink-getdestinationnode.md)
</dt> <dt>

[**контекстлинкдиректион**](contextlinkdirection.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

