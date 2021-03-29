---
description: Создает дочерний объект Иконтекстноде, который содержит только сведения о типе, идентификаторе и расположении.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'Метод Иконтекстноде:: Креатепартиаллипопулатедсубноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897490"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>Метод Иконтекстноде:: Креатепартиаллипопулатедсубноде

Создает дочерний объект [**иконтекстноде**](icontextnode.md) , который содержит только сведения о типе, идентификаторе и расположении.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнодетипе* \[ окне\]
</dt> <dd>

Тип создаваемого узла контекста.

</dd> <dt>

*пнодеид* \[ окне\]
</dt> <dd>

Идентификатор нового узла.

</dd> <dt>

*пноделокатион* \[ окне\]
</dt> <dd>

Расположение нового узла.

</dd> <dt>

*ппартиаллипопулатедконтекстнодекреатед* \[ заполняет\]
</dt> <dd>

Указатель на новое, частично заполненное [**иконтекстноде**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппартиаллипопулатедконтекстнодекреатед* , когда больше не нужно использовать контекстный узел.

 

Новый [**иконтекстноде**](icontextnode.md) добавляется в коллекцию дочерних узлов этого узла контекста (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)). При наличии существующих дочерних узлов вновь созданный **иконтекстноде** добавляется в качестве последнего дочернего узла.

Дополнительные сведения о типах, идентификаторах и расположении см. в разделе [**иконтекстноде:: GetType**](icontextnode-gettype.md), [**Иконтекстноде:: GetId**](icontextnode-getid.md)и [**иконтекстноде:: OnLocation**](icontextnode-getlocation.md).

Этот метод используется для прокси-сервера данных в качестве способа создания объекта [**иконтекстноде**](icontextnode.md) в дереве узлов контекста, прежде чем все сведения о нем доступны. Дополнительные сведения см. [в разделе Учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**ианалисисрегион**](ianalysisregion.md)
</dt> <dt>

[**Иконтекстноде:: Жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Типы узлов контекста](context-node-types.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

