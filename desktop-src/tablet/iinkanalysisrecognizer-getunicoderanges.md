---
description: Извлекает массив диапазонов символов, представляющих поддерживаемые диапазоны символов Юникода.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'Метод Иинканалисисрекогнизер:: Жетуникодеранжес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897474"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>Метод Иинканалисисрекогнизер:: Жетуникодеранжес

Извлекает массив диапазонов символов, представляющих поддерживаемые диапазоны символов Юникода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулнумберофранжес* \[ в, out\]
</dt> <dd>

Число диапазонов символов, на которые указывает *ппулловуникоде*.

</dd> <dt>

*ппулловуникоде* \[ заполняет\]
</dt> <dd>

Указатель на массив диапазонов символов, представляющий поддерживаемые диапазоны символов Юникода.

</dd> <dt>

*ппусуникодеранжеленгс* \[ заполняет\]
</dt> <dd>

Указатель на массив значений, указывающий длину каждой точки массива по *ппулловуникоде*.

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

[**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




