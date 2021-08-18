---
description: Извлекает варианты анализа для узлов в указанной коллекции Иконтекстнодес.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'Метод Иинканализер:: Жеталтернатесфорконтекстнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc282906bae70a28f612a8c1fd0a5a67ea1343c73f5ededf0d6c85a8bfd60aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939863"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>Метод Иинканализер:: Жеталтернатесфорконтекстнодес

Извлекает варианты анализа для узлов в указанной коллекции [**иконтекстнодес**](icontextnodes.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекстнодес* \[ окне\]
</dt> <dd>

Коллекция [**иконтекстнодес**](icontextnodes.md) , для которой возвращаются альтернативные варианты анализа.

</dd> <dt>

*улмаксимумалтернатес* \[ окне\]
</dt> <dd>

Максимальное число возвращаемых вариантов.

</dd> <dt>

*ппалтернатес* \[ заполняет\]
</dt> <dd>

Объект [**ианалисисалтернатес**](ianalysisalternates.md) , содержащий альтернативные варианты анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппалтернатес* , когда больше не нужно использовать объект.

 

Top [**ианалисисалтернате**](ianalysisalternate.md) возвращается в качестве первой альтернативы коллекции.

Объекты [**иконтекстноде**](icontextnode.md) в *пконтекстнодес* не должны представлять смежные области документа.

Для каждой подсказки по анализу в узлах [**иинканализер**](iinkanalyzer.md) возвращает только верхний альтернативный вариант.

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

[**ианалисисалтернате**](ianalysisalternate.md)
</dt> <dt>

[**ианалисисалтернатес**](ianalysisalternates.md)
</dt> <dt>

[**Метод Иинканализер:: Alternate**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Метод Иинканализер:: Жеталтернатесфорстрокес**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Модифитопалтернате**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Метод Иинканализер:: Модифитопалтернатевисконфирматион**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

