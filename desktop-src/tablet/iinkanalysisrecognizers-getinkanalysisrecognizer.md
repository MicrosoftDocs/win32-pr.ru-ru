---
description: Извлекает Иинканалисисрекогнизер по указанному индексу.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'Метод Иинканалисисрекогнизерс:: Жетинканалисисрекогнизер (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6755b82beaea1bec9a38b9c15ea57a97c1d19fc4eecb5a2b55c80e2070562d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967343"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>Метод Иинканалисисрекогнизерс:: Жетинканалисисрекогнизер

Извлекает [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) по указанному индексу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улиндекс* \[ окне\]
</dt> <dd>

Отсчитываемый от нуля индекс объекта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , который необходимо получить.

</dd> <dt>

*ппинканалисисрекогнизер* \[ заполняет\]
</dt> <dd>

Указатель на [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) по указанному индексу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппинканалисисрекогнизер* , когда больше не нужно использовать распознаватель рукописного анализа.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**инканалисисрекогнизерс**](iinkanalysisrecognizers.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

