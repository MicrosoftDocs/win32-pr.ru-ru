---
description: Выполняет синхронный анализ рукописного ввода.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Метод Иинканализер:: Analyze (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711118"
---
# <a name="iinkanalyzeranalyze-method"></a>Метод Иинканализер:: Analyze

Выполняет синхронный анализ рукописного ввода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппстатус* \[ заполняет\]
</dt> <dd>

Указатель на [**ианалисисстатус**](ianalysisstatus.md) , описывающий состояние операции анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппстатус* , когда больше не нужно использовать состояние анализа.

 

Этот метод запускает синхронную операцию анализа рукописного ввода. Анализ рукописного ввода включает в себя анализ макета, классификацию записи и рисования, а также распознавание рукописного ввода. Этот метод возвращает значение после завершения операции анализа.

Этот метод возвращает **\_ указатель E** , если *ппстатус* имеет **значение NULL**.

При вызове метода **иинканализер:: Analyze** или [**Иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md) [**иинканализер**](iinkanalyzer.md) анализирует рукописный ввод в пределах его «грязной» области (см. [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)). Однако **иинканализер** может расширить операцию анализа, включив в нее соседние регионы.

Этот метод задает для "грязной" области объекта [**иинканализер**](iinkanalyzer.md) пустую область. Если другой поток добавил данные Stroke, которые не были проанализированы, **иинканализер** добавляет ограничивающий прямоугольник необработанных штрихов в свою «грязную» область на этапе согласования анализа.

Этот метод возвращает ошибку, если приложение не обрабатывает событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) .

[**Иинканализер**](iinkanalyzer.md) не вызывает события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) и [**\_ ианалисисевентс:: интермедиатересултс**](-ianalysisevents-intermediateresults.md) в ответ на этот метод.

Чтобы изменить способ выполнения анализа рукописного ввода, используйте [**метод иинканализер:: сетаналисисмодес**](iinkanalyzer-setanalysismodes.md).

Дополнительные сведения о анализе рукописного ввода см. в разделе [Общие сведения об анализе рукописного текста](ink-analysis-overview.md).

## <a name="examples"></a>Примеры

В следующем примере выполняется фоновый анализ рукописного ввода.


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



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

[**аналисисмодес**](analysismodes.md)
</dt> <dt>

[**Метод Иинканализер:: Жетдиртирегион**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Метод Иинканализер:: Сетдиртирегион**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Метод Иинканализер:: Жетрутноде**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

