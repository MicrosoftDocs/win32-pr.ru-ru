---
description: Определяет, содержит ли указанный Ианалисисрегион значение, совпадающее с текущим объектом Ианалисисрегион.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'Метод Ианалисисрегион:: Екуалсрегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145562"
---
# <a name="ianalysisregionequalsregion-method"></a>Метод Ианалисисрегион:: Екуалсрегион

Определяет, содержит ли указанный [**ианалисисрегион**](ianalysisregion.md) значение, совпадающее с текущим объектом **ианалисисрегион** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*посеррегион* \[ окне\]
</dt> <dd>

Объект [**ианалисисрегион**](ianalysisregion.md) для сравнения с текущим **ианалисисрегион**.

</dd> <dt>

*пфрегионсекуал* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если указанный [**ианалисисрегион**](ianalysisregion.md) содержит то же значение, что и текущий ианалисисрегион; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисрегион**](ianalysisregion.md)
</dt> </dl>

 

 




