---
description: Сохраняет результаты анализа для определенной коллекции узлов контекста, связанной с Иинканализер.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'Метод Иинканализер:: Савересултсфорнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4386f9b051bf1cfcda6ee55d7b83728b096dc6f69de4d87745ce564f19249565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091574"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>Метод Иинканализер:: Савересултсфорнодес

Сохраняет результаты анализа для определенной коллекции узлов контекста, связанной с [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекстнодес* \[ окне\]
</dt> <dd>

Коллекция [**иконтекстноде**](icontextnode.md) , для которой необходимо сохранить результаты анализа.

</dd> <dt>

*пулсериализеддатасизе* \[ в, out\]
</dt> <dd>

Число байтов в *ппбсериализеддата*.

</dd> <dt>

*ппбсериализеддата* \[ заполняет\]
</dt> <dd>

Указатель на сериализованные данные анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для \* *ппбсериализеддата* , когда информация больше не нужна.

 

Этот метод сохраняет текущие результаты анализа для объектов [**иконтекстноде**](icontextnode.md) в *пконтекстнодес* и всех их предков и узлов контекста потомков. Этот метод не сохраняет данные росчерка. Приложение отвечает за синхронизацию результатов анализа и соответствующих данных штриха, если оно сохраняется.

Если объект [**иконтекстноде**](icontextnode.md) для сохранения заполняется только частично, этот метод возвращает код ошибки (см. [**Иконтекстноде:: жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Лоадресултс**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Метод Иинканализер:: Савересултс**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Метод Иинканализер:: Савересултсфорстрокес**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

