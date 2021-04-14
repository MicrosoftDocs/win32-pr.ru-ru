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
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542050"
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

## <a name="remarks"></a>Комментарии

Это значение задается методом [**иконтекстноде:: Confirm**](icontextnode-confirm.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Иконтекстноде:: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




