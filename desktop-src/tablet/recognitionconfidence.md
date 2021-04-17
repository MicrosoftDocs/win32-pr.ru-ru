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
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703203"
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

## <a name="remarks"></a>Комментарии

[**Иинканализер**](iinkanalyzer.md) использует один или несколько объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) для преобразования рукописного текста в текст.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Метод Ианалисисалтернате:: Жетрекогнитионконфиденце**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидата**](icontextnode-getpropertydata.md)
</dt> <dt>

[Свойства узла контекста](context-node-properties.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




