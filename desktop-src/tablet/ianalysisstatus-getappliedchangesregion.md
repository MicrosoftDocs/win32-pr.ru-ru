---
description: Извлекает регион документа, соответствующий изменениям, внесенным в дереве узлов контекста объекта Иинканализер в результате анализа рукописного ввода.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'Метод Ианалисисстатус:: Жетапплиедчанжесрегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3b2fec2528cbf961956e8b41f9eb6c985bd745d5dad097eb05544e64c42d122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044997"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>Метод Ианалисисстатус:: Жетапплиедчанжесрегион

Извлекает регион документа, соответствующий изменениям, внесенным в дереве узлов контекста объекта [**иинканализер**](iinkanalyzer.md) в результате анализа рукописного ввода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*папплиедчанжесрегион* \[ заполняет\]
</dt> <dd>

Указатель на [**ианалисисрегион**](ianalysisregion.md) документа, в котором были внесены изменения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *папплиедчанжесрегион* , когда больше не нужно использовать область анализа.

 

Этот метод чаще всего используется, когда приложение получает сведения для отладки и должно стать недействительным область, в которой могут возникнуть изменения, чтобы отрисовывать отладочную информацию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисстатус**](ianalysisstatus.md)
</dt> <dt>

[**ианалисисрегион**](ianalysisregion.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

