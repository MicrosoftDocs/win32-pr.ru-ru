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
ms.openlocfilehash: fd9a95ada1385fdbb6dbc5a1e22cde0ef319156ad7c3cd7782e911d06696af37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091564"
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

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для \* *ппбсериализеддата* , когда информация больше не нужна.

 

Этот метод сохраняет текущие результаты анализа для указанных штрихов. Этот метод сохраняет рукописные конечные объекты [**иконтекстноде**](icontextnode.md) , содержащие штрихи и все предки этих узлов контекста. Этот метод не сохраняет никаких данных штриха или узлов указания анализа. Приложение отвечает за синхронизацию результатов анализа и соответствующих данных штриха, если оно сохраняется.

Этот метод возвращает код ошибки, когда объект [**иконтекстноде**](icontextnode.md) для сохранения частично заполняется (см. [**Иконтекстноде:: жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)).

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

[**Метод Иинканализер:: Савересултсфорнодес**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

