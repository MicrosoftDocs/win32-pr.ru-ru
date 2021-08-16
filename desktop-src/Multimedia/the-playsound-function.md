---
title: Функция PlaySound
description: Функция PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- мультимедиа Audio, функция PlaySound
- Audio, функция PlaySound
- волна Audio, функция PlaySound
- PlaySound, функция
- Функция Сндплайсаунд
- PlaySound, функция по сравнению с функцией Сндплайсаунд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1921ec4ef91f6266b48ee80d7f42be4540124c0b5c98dc18438ce0d16c398c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370854"
---
# <a name="the-playsound-function"></a>Функция PlaySound

Функцию [**PlaySound**](/previous-versions//dd743680(v=vs.85)) можно использовать для воспроизведения звука звукозаписи, если звук умещается в доступную память. (Функция [**сндплайсаунд**](/previous-versions//dd798676(v=vs.85)) предлагает подмножество возможностей PlaySound. Чтобы максимально увеличить переносимость приложения на основе Win32, используйте **PlaySound**, а не **сндплайсаунд**.)

Функция **PlaySound** позволяет указать звук одним из трех способов:

-   В качестве системного предупреждения используйте псевдоним, хранящийся в файле WIN.INI или в реестре.
-   Как имя файла
-   Как идентификатор ресурса

Функция [**PlaySound**](/previous-versions//dd743680(v=vs.85)) позволяет воспроизводить звук в непрерывном цикле, заканчивая только при повторном вызове **PlaySound** , указывая **значение NULL** или идентификатор звука другого звука для параметра *псзсаунд* .

Функцию **PlaySound** можно использовать для синхронного или асинхронного воспроизведения звука, а также для управления поведением функции другими способами, когда она должна предоставлять общий доступ к системным ресурсам.

Дополнительные сведения об использовании функции PlaySound см. в следующих разделах:

-   [Использование функции PlaySound для воспроизведения Waveform-Audio файлов](using-playsound-to-play-waveform-audio-files.md)
-   [Использование функции PlaySound для цикла звуков](using-playsound-to-loop-sounds.md)
-   [Использование функции PlaySound для воспроизведения системных звуков](using-playsound-to-play-system-sounds.md)

Дополнительные примеры использования **PlaySound** в приложениях на основе Win32 см. в разделе [Воспроизведение звуковых ресурсов](playing-wave-resources.md).

 

 