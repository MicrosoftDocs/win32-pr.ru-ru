---
description: Извлекает значение, указывающее, представляет ли Ианалисисрегион неограниченную область.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'Метод Ианалисисрегион:: Infinite (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263160"
---
# <a name="ianalysisregionisinfinite-method"></a>Метод Ианалисисрегион:: Infinite

Извлекает значение, указывающее, представляет ли [**ианалисисрегион**](ianalysisregion.md) неограниченную область.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфисинфините* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если представленный регион является бесконечным; в противном случае — **\_ значение false**.

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
</dt> <dt>

[**Метод Ианалисисрегион:: IsEmpty**](ianalysisregion-isempty.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Макимпти**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Макеинфините**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




