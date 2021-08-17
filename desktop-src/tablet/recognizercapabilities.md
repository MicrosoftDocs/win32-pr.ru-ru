---
description: Задает атрибуты Иинканалисисрекогнизер.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Перечисление Рекогнизеркапабилитиес (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 96e932b8e47f323198e1b0cc87da0df7839a593a76850c00c2c2e4d095854851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091454"
---
# <a name="recognizercapabilities-enumeration"></a>Перечисление Рекогнизеркапабилитиес

Задает атрибуты [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**Версия-кандидат \_ None**
</dt> <dd>

Возможности не указаны.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**Версия-кандидат \_ доноткаре**
</dt> <dd>

Игнорирует все установленные флаги.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC, \_ объект**
</dt> <dd>

Поддерживает распознавание объектов; в противном случае распознает только текст.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**Версия-кандидат \_ фриинпут**
</dt> <dd>

Поддерживает свободные входные данные, в которых рукописные данные записываются без использования руководств по распознаванию, например линии или поля.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**Версия-кандидат \_ линединпут**
</dt> <dd>

Поддерживает линейный ввод, аналогичный написанию на бумаге.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**Версия-кандидат \_ боксединпут**
</dt> <dd>

Поддерживает Упакованные входные данные, где каждый символ или слово введены в поле.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**Версия-кандидат \_ чарактераутокомплетионинпут**
</dt> <dd>

Поддерживает автозаполнение символов. Распознаватели, поддерживающие Автозаполнение символов, нуждаются в упакованных входных данных.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**Версия-кандидат \_ ригхтанддовн**
</dt> <dd>

Поддерживает ввод рукописного ввода в правильном и меньшом порядке, например в западных языках и на некоторых восточно-азиатских языках.

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**Версия-кандидат \_ лефтанддовн**
</dt> <dd>

Поддерживает рукописный ввод в левом и меньшом порядке, например на иврите и арабском языке.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**Версия-кандидат \_ довнандлефт**
</dt> <dd>

Поддерживает рукописный ввод в порядке вниз и слева, например на некоторых восточно-азиатских языках.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**Версия-кандидат \_ довнандригхт**
</dt> <dd>

Поддерживает ввод рукописного ввода в неправильном порядке, например на некоторых восточно-азиатских языках.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**Версия-кандидат \_ арбитрарянгле**
</dt> <dd>

Поддерживает текст, написанный в произвольных угловах.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**Версия-кандидат \_ Lattice**
</dt> <dd>

Поддерживает возврат Lattice в качестве альтернативы строки для результатов распознавания рукописного текста.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**Версия-кандидат \_ адвисеинкчанже**
</dt> <dd>

Поддерживает прерывание распознавания фона, например изменение рукописного ввода.

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**Версия-кандидат \_ строкереордер**
</dt> <dd>

Поддерживает этот порядок штрихов, пространственный и временный, который обрабатывается как часть операции распознавания. [**Иинканализер**](iinkanalyzer.md) не переупорядочивает штрихи перед отправкой рукописного ввода в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**\_Настраиваемый RC**
</dt> <dd>

Поддерживает персонализированный рукописный ввод, при котором распознаватель улучшает распознавание при использовании рукописного ввода с течением времени.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**Версия-кандидат \_ преферсарбитрарянгле**
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) не нужно поворачивать рукописный текст на горизонтальную ориентацию перед отправкой рукописного ввода в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**Версия-кандидат \_ преферспараграфбреакинг**
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) должен отправить в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)целые абзацы рукописного ввода, позволяя **иинканалисисрекогнизер** выполнить разрыв строки и слово (или знак).

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**Версия-кандидат \_ преферссегментатионрекогнитион**
</dt> <dd>

Распознает только одно слово или символ для каждой операции распознавания. [**Иинканализер**](iinkanalyzer.md) выполняет сегментацию на рукописном тексте и отправляет в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)только один сегмент.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление позволяет побитовое сочетание значений его членов. Используйте это перечисление, чтобы найти установленный распознаватель рукописного ввода, который поддерживает необходимые атрибуты.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Возможности Иинканалисисрекогнизер:: Capabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




