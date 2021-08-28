---
description: Извлекает все объекты Иконтекстноде указанного типа.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'Метод Иинканализер:: Финднодесофтипе (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ab35825c47ddbbdeda3affc0ab0585dce111233990db28ae65a0636f7145ce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939963"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a>Метод Иинканализер:: Финднодесофтипе

Извлекает все объекты [**иконтекстноде**](icontextnode.md) указанного типа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнодетипе* \[ окне\]
</dt> <dd>

**Идентификатор GUID** , указывающий тип узла.

</dd> <dt>

*ппконтекстнодесфаунд* \[ заполняет\]
</dt> <dd>

Указатель на [**иконтекстнодес**](icontextnodes.md) , содержащий все узлы типа *пнодетипе*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.

 

Свойство *пнодетипе* должно содержать идентификатор GUID из констант [типов узлов контекста](context-node-types.md) .

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

[**Метод Иинканализер:: Финднодесофтипефорстрокес**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесофтипеинсубтри**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесвискаллбакк**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

