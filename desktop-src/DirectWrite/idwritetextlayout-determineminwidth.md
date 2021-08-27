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
ms.openlocfilehash: 41123f2a5d584341c344248d0af936f34fc04e49c9aabc1cb73ecea0eacc84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075534"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дврите. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

