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
ms.openlocfilehash: 7233c6e0303f0634c71a67fde13f237feb2b2f6c6518dd8edc0b1624b4e2b6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940294"
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

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппартиаллипопулатедконтекстнодекреатед* , когда больше не нужно использовать контекстный узел.

 

Новый [**иконтекстноде**](icontextnode.md) добавляется в коллекцию дочерних узлов этого узла контекста (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)). При наличии существующих дочерних узлов вновь созданный **иконтекстноде** добавляется в качестве последнего дочернего узла.

Дополнительные сведения о типах, идентификаторах и расположении см. в разделе [**иконтекстноде:: GetType**](icontextnode-gettype.md), [**Иконтекстноде:: GetId**](icontextnode-getid.md)и [**иконтекстноде:: OnLocation**](icontextnode-getlocation.md).

Этот метод используется для прокси-сервера данных в качестве способа создания объекта [**иконтекстноде**](icontextnode.md) в дереве узлов контекста, прежде чем все сведения о нем доступны. Дополнительные сведения см. [в разделе Учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requirements (Требования)



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

[**ианалисисрегион**](ianalysisregion.md)
</dt> <dt>

[**Иконтекстноде:: Жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Типы узлов контекста](context-node-types.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

