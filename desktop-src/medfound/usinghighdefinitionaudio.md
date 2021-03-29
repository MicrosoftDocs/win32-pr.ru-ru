---
description: Использование High-Definition Audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Использование High-Definition Audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812580"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Использование High-Definition Audio (Microsoft Media Foundation)

Высококачественное аудио, в контексте кодеков Windows Media Audio, — это любой тип звука с более чем двумя каналами или более 16 бит на выборку. Высококачественное аудио поддерживается в категориях "профессиональная" и "без потерь" [кодировщика Windows Media Audio](windowsmediaaudioencoder.md).

Несжатые звуковые типы высокой четкости определяются с помощью структуры [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) . **Вавеформатекстенсибле** — это структурированное расширение структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) . При использовании дмос элемент **форматтипе** структуры [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) , описывающий тип звука высокой четкости, должен иметь значение вмкформат \_ вавеформатекс, как и для обычного звука; для **вавеформатекстенсибле** не существует специального идентификатора формата. Если в формате используется **вавеформатекстенсибле** , необходимо задать для элемента **кбсизе** структуры **вавеформатекс** значение 22.

При использовании Media Foundation можно создать правильный тип мультимедиа из структуры [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) с помощью функции [**мфинитмедиатипефромвавеформатекс**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).

Многоканальные типы вывода, поддерживаемые кодеком Windows Media Audio 10 Professional, не используют [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), но сообщают правильное количество каналов и бит на выборку в структуре [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) . Как и для всех типов аудио, описывающих сжатое аудио-содержимое Windows Media, в структуру **вавеформатекс** , используемую декодером для распаковки, добавлены дополнительные сведения.

## <a name="decoding-high-definition-audio"></a>Декодирование High-Definition аудио

Для расшифровки звука высокой четкости необходимо задать для свойства [мфпкэй \_ вмадек \_ хиресаутпут](mfpkey-wmadec-hiresoutputproperty.md) значение Variant \_ true. Если это свойство не задано, декодер будет доставлять стерео-содержимое максимум 16 бит на выборку независимо от сжатого формата.

> [!Note]  
> High-Definition Audio поддерживается только для Windows XP, Windows Vista и более поздних версий. В более ранних версиях Windows аудио-содержимое Windows Media, закодированное с помощью High Definition, отображается в виде двухканального звука с максимум 16 бит на выборку.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Работа с аудио](workingwithaudio.md)
</dt> </dl>

 

 
