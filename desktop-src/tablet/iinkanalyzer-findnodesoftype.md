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
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897458"
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

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.

 

Свойство *пнодетипе* должно содержать идентификатор GUID из констант [типов узлов контекста](context-node-types.md) .

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

 

