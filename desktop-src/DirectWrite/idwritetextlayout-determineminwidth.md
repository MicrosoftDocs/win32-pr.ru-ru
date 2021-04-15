---
title: Идвритетекстлайаут Детерминеминвидс, метод
description: Определяет минимальную возможную ширину, на которую можно установить макет без аварийного разрыва между символами целых слов.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Непосредственная запись метода Детерминеминвидс
- Прямая запись метода Детерминеминвидс, интерфейс Идвритетекстлайаут
- Прямая запись интерфейса Идвритетекстлайаут, метод Детерминеминвидс
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689024"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>Идвритетекстлайаут: метод:D Етерминеминвидс

Определяет минимальную возможную ширину, на которую можно установить макет без аварийного разрыва между символами целых слов.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*minWidth* \[ заполняет\]
</dt> <dd>

Тип: **float \***

Минимальная ширина.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

 

