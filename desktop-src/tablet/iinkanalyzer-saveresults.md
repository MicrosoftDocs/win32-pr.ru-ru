---
description: Сохраняет все результаты анализа для Иинканализер.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'Метод Иинканализер:: Савересултс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 216f238776cf88a24d10f57671aa4f03c71d07962ff480d5b219653a5c9d338e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091994"
---
# <a name="iinkanalyzersaveresults-method"></a>Метод Иинканализер:: Савересултс

Сохраняет все результаты анализа для [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулсериализеддатасизе* \[ заполняет\]
</dt> <dd>

Число байтов в *ппбсериализеддата*.

</dd> <dt>

*ппбсериализеддата* \[ заполняет\]
</dt> <dd>

Массив, содержащий сохраненные результаты анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппбсериализеддата* , если эта информация больше не нужна.

 

Этот метод сохраняет все текущие результаты анализа, включая текущую подсказку анализа и пользовательские узлы распознавателя (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md)). Этот метод не сохраняет данные росчерка. При сохранении данных приложение отвечает за синхронизацию результатов анализа и соответствующих штрихов.

Этот метод возвращает код ошибки, когда объект [**иконтекстноде**](icontextnode.md) для сохранения частично заполняется (см. [**Иконтекстноде:: жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)).

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

[**Метод Иинканализер:: Лоадресултс**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Метод Иинканализер:: Савересултсфорнодес**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**Метод Иинканализер:: Савересултсфорстрокес**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

