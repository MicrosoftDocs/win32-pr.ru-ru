---
description: Возвращает объекты Иконтекстноде, связанные с этим альтернативным.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'Метод Ианалисисалтернате:: Жеталтернатенодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fbaff3cea515c9636127ce2267b9f05e0c0a0006b96046a7f2474661b3b76f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935524"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>Метод Ианалисисалтернате:: Жеталтернатенодес

Возвращает объекты [**иконтекстноде**](icontextnode.md) , связанные с этим альтернативным.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппалтернатенодес* \[ заполняет\]
</dt> <dd>

Указатель на коллекцию [**иконтекстнодес**](icontextnodes.md) , содержащую объекты [**иконтекстноде**](icontextnode.md) , связанные с этим альтернативным.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппалтернатенодес* , когда больше не нужно использовать коллекцию узлов контекста.

 

Этот метод возвращает конечные узлы контекста, связанные с этим альтернативным. Примерами конечных узлов являются узлы контекста Инкворд, Текстворд, Image, Инкдравинг и Инкбуллет. Дополнительные сведения см. в разделе [**иконтекстноде:: GetType**](icontextnode-gettype.md) и [типы узлов контекста](context-node-types.md).

Так как они соответствуют альтернативным объектам, эти объекты [**иконтекстноде**](icontextnode.md) не являются потомками корневого **иконтекстноде** объекта [**Иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md)), если только они не являются верхним вариантом, который является первым элементом в коллекции [**ианалисисалтернатес**](ianalysisalternates.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ианалисисалтернате**](ianalysisalternate.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**иконтекстнодес**](icontextnodes.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> <dt>

[Системой. Windows. Ink. Аналисискоре. Аналисисалтернатебасе. Алтернатенодес](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

