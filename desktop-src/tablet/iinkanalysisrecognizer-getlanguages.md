---
description: Получает идентификаторы для языковых стандартов, которые поддерживает эта Иинканалисисрекогнизер.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: Метод иинканалисисрекогнизер::-languageing (иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897477"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>Метод Иинканалисисрекогнизер:: WebMethod

Получает идентификаторы для языковых стандартов, которые поддерживает эта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пуллангуажескаунт* \[ в, out\]
</dt> <dd>

Число идентификаторов в *ппуллангуажес*.

</dd> <dt>

*ппуллангуажес* \[ заполняет\]
</dt> <dd>

Указатель на идентификаторы языковых стандартов, которые поддерживает эта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппуллангуажес* , если эта информация больше не нужна.

 

Этот метод возвращает пустой массив для распознавателей объектов и жестов.

Дополнительные сведения об идентификаторах языков см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).

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
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

