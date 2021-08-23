---
description: Извлекает значение, указывающее, задан ли для этого Иконтекстноде Конфирматионтипе, переданный этому методу.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'Метод Иконтекстноде:: Confirm (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2e378aaf344e177514115c82b1179f8d1ebe25faefa0d5d840d5a0af62ff1c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967363"
---
# <a name="icontextnodeisconfirmed-method"></a>Метод Иконтекстноде:: Confirm

Извлекает значение, указывающее, задан ли для этого Иконтекстноде Конфирматионтипе, переданный этому методу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*конфирмедтипе* \[ окне\]
</dt> <dd>

Проверяемый тип подтверждения.

</dd> <dt>

*пфтипеконфирмед* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если для этого объекта [**иконтекстноде**](icontextnode.md) был задан тип, переданный в конфирмедтипе; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Это значение задается методом [**иконтекстноде:: Confirm**](icontextnode-confirm.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Иконтекстноде:: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




