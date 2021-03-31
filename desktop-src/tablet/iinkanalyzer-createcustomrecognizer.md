---
description: Создает новый пользовательский узел распознавателя для Иинканализер.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'Метод Иинканализер:: Креатекустомрекогнизер (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263144"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a>Метод Иинканализер:: Креатекустомрекогнизер

Создает новый пользовательский узел распознавателя для [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканалисисрекогнизерид* \[ окне\]
</dt> <dd>

Глобальный уникальный идентификатор (GUID) [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , для которого создается узел.

</dd> <dt>

*ппконтекстноде* \[ заполняет\]
</dt> <dd>

Указатель на объект [**иконтекстноде**](icontextnode.md) , представляющий новый пользовательский узел распознавателя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в ппконтекстноде, когда больше не нужно использовать объект.

 

Этот метод создает новый [**иконтекстноде**](icontextnode.md) с типом кустомрекогнизер (см. [**Иконтекстноде:: GetType**](icontextnode-gettype.md)). Затем он добавляет новый пользовательский узел распознавателя в коллекцию подузлов корневого узла объекта [**иинканализер**](iinkanalyzer.md) (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) and [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md)).

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

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

