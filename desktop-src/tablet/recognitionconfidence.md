---
description: Указывает уровень достоверности, в котором Иинканализер имеет точность результата распознавания.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Перечисление Рекогнитионконфиденце (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b5943b303c01a681b1df9d6d919df1822a5f2345c85fb5c52e3ab865ee58dd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596634"
---
# <a name="recognitionconfidence-enumeration"></a>Перечисление Рекогнитионконфиденце

Указывает уровень достоверности, в котором [**иинканализер**](iinkanalyzer.md) имеет точность результата распознавания.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**Рекогнитионконфиденце \_ strong**
</dt> <dd>

Надежная уверенность в результатах или альтернативном варианте.

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**\_Промежуточный рекогнитионконфиденце**
</dt> <dd>

Промежуточная уверенность в результате или в альтернативном варианте.

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**Рекогнитионконфиденце \_ плохо**
</dt> <dd>

Низкая уверенность в результатах или альтернативе.

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**Рекогнитионконфиденце \_ неизвестный**
</dt> <dd>

[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , создавший распознанный текст, не поддерживает уровни достоверности.

</dd> </dl>

## <a name="remarks"></a>Remarks

[**Иинканализер**](iinkanalyzer.md) использует один или несколько объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) для преобразования рукописного текста в текст.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Метод Ианалисисалтернате:: Жетрекогнитионконфиденце**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидата**](icontextnode-getpropertydata.md)
</dt> <dt>

[Свойства узла контекста](context-node-properties.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




