---
description: Извлекает область, которая изменилась со времени последнего выполнения операции анализа.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'Метод Иинканализер:: Жетдиртирегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263140"
---
# <a name="iinkanalyzergetdirtyregion-method"></a>Метод Иинканализер:: Жетдиртирегион

Извлекает область, которая изменилась со времени последнего выполнения операции анализа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдиртирегион* \[ заполняет\]
</dt> <dd>

Объект [**ианалисисрегион**](ianalysisregion.md) , описывающий область, измененную с момента последнего выполнения операции анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппдиртирегион* , когда больше не нужно использовать объект.

 

Этот метод определяет области, которые необходимо проанализировать или повторно проанализировать. Все методы [**иинканализер**](iinkanalyzer.md) , которые добавляют, обновляют или удаляют данные обводки, обновляют «грязную» область. Чтобы вручную пометить область для переанализа:

1.  Получите "грязную" область с помощью **метода иинканализер:: жетдиртирегион**.
2.  Используйте [**метод ианалисисрегион:: унионрегион**](ianalysisregion-unionregion.md) или [**метод Ианалисисрегион:: унионректангле**](ianalysisregion-unionrectangle.md) для добавления области в регион из шага 1.
3.  Чтобы обновить "грязную" область, используйте [**метод иинканализер:: сетдиртирегион**](iinkanalyzer-setdirtyregion.md) .

[**Иинканализер**](iinkanalyzer.md) анализирует рукописный ввод в своей «грязной» области во время вызова метода [**Иинканализер:: Analyze**](iinkanalyzer-analyze.md) или [**иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md). Однако **иинканализер** может расширить операцию анализа, включив в нее соседние регионы.

Это свойство может содержать несмежные области.

Используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память из массива *ппдиртирегион* по завершении работы с ним.

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

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстроке**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокес**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокесфорлангуаже**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Ремовестроке**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Метод Иинканализер:: Ремовестрокес**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Упдатестрокесдата**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

