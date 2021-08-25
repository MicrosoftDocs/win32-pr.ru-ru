---
description: Завершает все необходимые операции в буфере метаданных и освобождает указанный объект Испатиалаудиометадатаитемс.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'Метод Испатиалаудиометадатавритер:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 4b29efb38cf11ba718a631f676323eb3db93aab042c70691dfb89ce957266e86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875424"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>Метод Испатиалаудиометадатавритер:: Close

Завершает все необходимые операции в буфере метаданных и освобождает указанный объект [**испатиалаудиометадатаитемс**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Close();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае неудачи возможные коды возврата включают, но не ограничиваются значениями, приведенными в следующей таблице.



| Код возврата                                                                                                                     | Описание                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**СПТЛАУД \_ MD \_ клнт \_ E \_ нет \_ \_ открытых элементов**</dt> </dl>            | Предоставленный [**испатиалаудиометадатаитемс**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) не был открыт с помощью вызова [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).<br/> |
| <dl> <dt>**СПТЛАУД \_ MD \_ клнт \_ E \_ не \_ \_ записано элементов**</dt> </dl>         | Не были записаны элементы метаданных в предоставленный [**испатиалаудиометадатаитемс**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).<br/>                                              |
| <dl> <dt>**\_элемент сптлауд MD \_ клнт \_ E \_ \_ должен \_ иметь \_ команды**</dt> </dl> | В предоставленный [**испатиалаудиометадатаитемс**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)не записаны команды метаданных.<br/>                                           |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**испатиалаудиометадатавритер**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




