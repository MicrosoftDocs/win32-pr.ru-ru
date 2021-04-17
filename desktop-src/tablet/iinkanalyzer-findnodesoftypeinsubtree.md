---
description: Извлекает все объекты Иконтекстноде указанного типа, являющиеся потомками указанного объекта Иконтекстноде.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'Метод Иинканализер:: Финднодесофтипеинсубтри (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 545e56d297b053b5b6f5dc61f944d6a4f6d4e03c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711113"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a>Метод Иинканализер:: Финднодесофтипеинсубтри

Извлекает все объекты [**иконтекстноде**](icontextnode.md) указанного типа, являющиеся потомками указанного объекта **иконтекстноде** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнодетипе* \[ окне\]
</dt> <dd>

**Идентификатор GUID** , указывающий тип узла.

</dd> <dt>

*пконтекстнодетосеарчфром* \[ окне\]
</dt> <dd>

Объект [**иконтекстноде**](icontextnode.md) , потомки которого ищутся.

</dd> <dt>

*ппконтекстнодесфаунд* \[ заполняет\]
</dt> <dd>

Коллекция [**иконтекстнодес**](icontextnodes.md) , содержащая все узлы типа *пнодетипе* , которые являются потомками *пконтекстнодетосеарчфром*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.

 

Если [**иинканализер**](iinkanalyzer.md) не содержит узел *пконтекстнодетосеарчфром* , этот метод возвращает код ошибки.

Свойство *пнодетипе* должно содержать глобальный уникальный идентификатор (GUID) из констант [типов узлов контекста](context-node-types.md) .

Если [**иинканализер**](iinkanalyzer.md) не содержит таких [**иконтекстноде**](icontextnode.md), возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Финдинклеафнодес**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**Метод Иинканализер:: Финдинклеафнодесфорстрокес**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Финдлеафнодес**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Метод Иинканализер:: Финдноде**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесофтипе**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесофтипефорстрокес**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесвискаллбакк**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

