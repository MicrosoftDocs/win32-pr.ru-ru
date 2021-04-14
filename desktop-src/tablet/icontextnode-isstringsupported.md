---
description: Указывает, поступил ли распознанная строка этого Иконтекстноде из системного словаря, пользовательского словаря или списка слов.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'Метод Иконтекстноде:: Исстрингсуппортед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692437"
---
# <a name="icontextnodeisstringsupported-method"></a>Метод Иконтекстноде:: Исстрингсуппортед

Указывает, поступил ли распознанная строка этого [**иконтекстноде**](icontextnode.md) из системного словаря, пользовательского словаря или списка слов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфиссуппортед* \[ out, retval\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если распознанное строковое значение данного [**Иконтекстноде**](icontextnode.md) поддерживается [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) с любыми соответствующими узлами подсказок. в противном случае — **\_ значение false**.

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

[**иконтекстноде**](icontextnode.md)
</dt> </dl>

 

 




