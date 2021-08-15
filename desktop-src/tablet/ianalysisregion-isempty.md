---
description: Получает значение, указывающее, представляет ли Ианалисисрегион пустой регион.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'Метод Ианалисисрегион:: IsEmpty (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a599d88371a1a6726ed2ec4ee217c36b3ea3cd71d6117305a59860cb9a8bf09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092325"
---
# <a name="ianalysisregionisempty-method"></a>Метод Ианалисисрегион:: IsEmpty

Получает значение, указывающее, представляет ли [**ианалисисрегион**](ianalysisregion.md) пустой регион.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфисемпти* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если представленный регион пуст; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисрегион**](ianalysisregion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Infinite**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Макимпти**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Макеинфините**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




