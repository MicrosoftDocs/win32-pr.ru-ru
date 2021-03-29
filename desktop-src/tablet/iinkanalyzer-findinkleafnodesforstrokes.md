---
description: Получает конечные узлы рукописного ввода, содержащие указанные штрихи.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'Метод Иинканализер:: Финдинклеафнодесфорстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897461"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>Метод Иинканализер:: Финдинклеафнодесфорстрокес

Получает конечные узлы рукописного ввода, содержащие указанные штрихи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улстрокеидскаунт* \[ окне\]
</dt> <dd>

Число переданных идентификаторов Stroke.

</dd> <dt>

*плстрокеидс* \[ окне\]
</dt> <dd>

Массив идентификаторов Stroke.

</dd> <dt>

*ппконтекстнодесфаунд* \[ заполняет\]
</dt> <dd>

Коллекция объектов [**иконтекстноде**](icontextnode.md) , которая содержит все конечные узлы рукописного ввода, содержащие штрихи с идентификаторами в массиве *плстрокеидс* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.

 

Конечные узлы не содержат дочерних узлов. Узлы рукописного ввода содержат данные Stroke. Примерами перьевых узлов являются Инкворд, Инкдравинг, Андинкбуллет [**иконтекстноде**](icontextnode.md) . Дополнительные сведения см. в разделе [типы узлов контекста](context-node-types.md).

Если ни один из узлов не содержит указанных штрихов, возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) . Аналогично, если *улстрокеидскаунт* равен нулю, возвращается пустая коллекция **иконтекстнодес** .

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

[**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

