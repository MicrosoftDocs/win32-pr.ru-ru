---
title: Идвритетекстлайаут Жетоверхангметрикс, метод
description: Возвращает перестает отвечать (в DIP) макета и всех содержащихся в нем объектов, включая текстовые глифы и встроенные объекты.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Непосредственная запись метода Жетоверхангметрикс
- Прямая запись метода Жетоверхангметрикс, интерфейс Идвритетекстлайаут
- Прямая запись интерфейса Идвритетекстлайаут, метод Жетоверхангметрикс
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3591df5dc02fdc63215ff2276202df62347ed21aef23991b4ddcadef094281
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649749"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>Метод Идвритетекстлайаут:: Жетоверхангметрикс

Возвращает перестает отвечать (в DIP) макета и всех содержащихся в нем объектов, включая текстовые глифы и встроенные объекты.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*перестает отвечать* \[ заполняет\]
</dt> <dd>

Тип: **[ **двритеные \_ \_ метрики выступа**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Прокрутка видимых экстентов (в DIP) за пределами макета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Подчеркивания и зачеркивание не влияют на определение черного прямоугольника, поскольку они на самом деле рисуются модулем подготовки отчетов, который может нарисовать их в различных стилях.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дврите. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

