---
description: Сохраняет результаты анализа для указанных штрихов, связанных с Иинканализер.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'Метод Иинканализер:: Савересултсфорстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343675"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>Метод Иинканализер:: Савересултсфорстрокес

Сохраняет результаты анализа для указанных штрихов, связанных с [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улстрокеидскаунт* \[ окне\]
</dt> <dd>

Число идентификаторов Stroke в **плстрокеидс**.

</dd> <dt>

*плстрокеидс* \[ окне\]
</dt> <dd>

Массив идентификаторов Stroke.

</dd> <dt>

*пулсериализеддатасизе* \[ в, out\]
</dt> <dd>

Число байтов в *ппбсериализеддата*.

</dd> <dt>

*ппбсериализеддата* \[ out, retval\]
</dt> <dd>

Указатель на сериализованные данные анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для \* *ппбсериализеддата* , когда информация больше не нужна.

 

Этот метод сохраняет текущие результаты анализа для указанных штрихов. Этот метод сохраняет рукописные конечные объекты [**иконтекстноде**](icontextnode.md) , содержащие штрихи и все предки этих узлов контекста. Этот метод не сохраняет никаких данных штриха или узлов указания анализа. Приложение отвечает за синхронизацию результатов анализа и соответствующих данных штриха, если оно сохраняется.

Этот метод возвращает код ошибки, когда объект [**иконтекстноде**](icontextnode.md) для сохранения частично заполняется (см. [**Иконтекстноде:: жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)).

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

[**Метод Иинканализер:: Лоадресултс**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Метод Иинканализер:: Савересултс**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Метод Иинканализер:: Савересултсфорнодес**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

