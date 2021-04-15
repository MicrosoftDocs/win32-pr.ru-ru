---
description: Указывает, получена ли указанная распознанная строка из системного словаря, пользовательского словаря или списка слов.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'Метод Иконтекстноде:: Исалтернатестрингсуппортед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662407"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>Метод Иконтекстноде:: Исалтернатестрингсуппортед

Указывает, получена ли указанная распознанная строка из системного словаря, пользовательского словаря или списка слов. Для определения того, поддерживается ли строка, можно использовать любые ограниченные данные, такие как списков слов, направляющих или фактоидс, в любом соответствующем узле подсказок.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстралтернатестринг* \[ окне\]
</dt> <dd>

Распознанная строка для проверки.

</dd> <dt>

*пфиссуппортед* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если указанная строка поддерживается [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) с любыми соответствующими узлами подсказок; **Вариант \_ Значение FALSE** , если не поддерживается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

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

 

 




