---
description: Извлекает все объекты Иконтекстноде, соответствующие заданным критериям, и являются потомками указанного объекта Иконтекстноде.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'Метод Иинканализер:: Финднодесвискаллбаккинсубтри (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d6ab8e66e75af4e31a1efacd082f79f68d5f63c546c56d59bf4ca0fedc201929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939934"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>Метод Иинканализер:: Финднодесвискаллбаккинсубтри

Извлекает все объекты [**иконтекстноде**](icontextnode.md) , соответствующие заданным критериям, и являются потомками указанного объекта **иконтекстноде** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкритериа* \[ окне\]
</dt> <dd>

Объект [**иматческритериакаллбакк**](imatchescriteriacallback.md) , используемый для вычисления того, соответствует ли объект [**иконтекстноде**](icontextnode.md) заданным условиям или не завершается.

</dd> <dt>

*пконтекстнодетосеарчфром* \[ окне\]
</dt> <dd>

Объект [**иконтекстноде**](icontextnode.md) , потомки которого ищутся.

</dd> <dt>

*ппконтекстнодесфаунд* \[ заполняет\]
</dt> <dd>

Указатель на [**иконтекстнодес**](icontextnodes.md) , содержащий все узлы, соответствующие заданным критериям.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.

 

Если [**иинканализер**](iinkanalyzer.md) не содержит узел *пконтекстнодетосеарчфром* , этот метод возвращает код ошибки.

Если [**иинканализер**](iinkanalyzer.md) не содержит таких [**иконтекстноде**](icontextnode.md), возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

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

[**Метод Иинканализер:: Финднодесофтипеинсубтри**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесвискаллбакк**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

