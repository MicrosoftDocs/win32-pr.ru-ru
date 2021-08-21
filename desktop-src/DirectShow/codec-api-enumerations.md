---
description: Перечисления API кодеков
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: Перечисления API кодеков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28b82d73d6bd6fefed5f3c9296a666d1053cd71b074a782858b31e94dc3a3ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079334"
---
# <a name="codec-api-enumerations"></a>Перечисления API кодеков



| Перечисление                                                                              | Описание                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**еаваудиочаннелконфиг**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | Задает конфигурацию динамика для каналов звука в потоке звукового бита.                       |
| [**еавддсурраундмоде**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | Указывает, кодируется ли звук в окружающее окружение Dolby.                                                 |
| [**еавдекаакдовнмиксмоде**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | Указывает, использует ли декодер AAC стандартные уравнения MPEG-2/MPEG-4 стерео довнмикс.                    |
| [**еавдекаудиодуалмоно**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | Указывает, имеет ли входной поток ввода стерео или Dual Mono.                                          |
| [**еавдекаудиодуалмонорепромоде**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | Указывает, как декодер воспроизводит два моно аудио.                                                     |
| [**еавдекддоператионалмоде**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | Задает режим управления сжатием для звукового потока Dolby AC-3.                                     |
| [**еавдечеаакдинамикранжеконтрол**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | Указывает, выполняет ли декодер AAC динамическое управление диапазонами.                                          |
| [**еавдеквидеоинпутскантипе**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | Указывает способ чередования декодированного видео-потока.                                                     |
| [**еавдеквидеософтваредеинтерлацемоде**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | Указывает режим программной развертки для видеодекодера.                                                    |
| [**еавдеквидеосвповерлевел**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | Задает уровень энергосбережения видеодекодера.                                                      |
| [**еавдсплауднессекуализатион**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | Указывает, включено ли обравенство громкости в звуковом декодере или в поставщике цифровых сигналов (DSP). |
| [**еавдспспеакерфилл**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | Указывает, включена ли заливка динамиков в аудио-декодере или в DSP.                                     |
| [**еавенкаудиодуалмоно**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | Указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono.                                      |
| [**Перечисление Еавенкаудиоинпутконтент**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | Указывает, содержит ли аудио содержимое музыку или голос.                                              |
| [**еавенккоммонратеконтролмоде**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | Задает режим управления скоростью.                                                                          |
| [**еавенккоммонстреамендхандлинг**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | Указывает, отбрасывает ли кодировщик частичные группы изображений (группы GOP) в конце потока.        |
| [**еавенкддатодконвертертипе**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | Указывает тип преобразования аналогово в цифровое (A/D) для потока цифрового звука Dolby.                |
| [**еавенкдддинамикранжекомпрессионконтрол**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | Задает динамический профиль управления диапазоном в потоке цифрового звука Dolby.                              |
| [**еавенкддхеадфонемоде**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | Указывает режим наушников для потока цифрового звука Dolby.                                                |
| [**еавенкддпреферредстереодовнмиксмоде**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | Указывает предпочитаемый режим стерео довнмикс для потока цифрового аудио Dolby.                             |
| [**еавенкддпродуктионрумтипе**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | Указывает тип комнаты для потока цифрового аудио Dolby.                                                 |
| [**еавенкддсервице**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | Указывает службу аудио, которая содержится в потоке цифрового звука Dolby.                                    |
| [**еавенкддсурраундексмоде**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | Указывает, кодируется ли поток цифрового звука Dolby в цифровом окружении Dolby, например.                   |
| [**еавенЦинпутвидеосистем**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | Указывает Номинальный диапазон для источника видео.                                                           |
| [**еавенкмпакодингмоде**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | Указывает режим кодирования звука MPEG.                                                                   |
| [**еавенкмпаемфасистипе**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | Указывает тип фильтра отмены выделения, который должен использоваться при декодировании.                               |
| [**еавенкмпалайер**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | Задает звуковой слой MPEG.                                                                           |
| [**еавенкмпвфрамефиелдмоде**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | Указывает, создает ли кодировщик закодированные поля или закодированные фреймы.                                  |
| [**еавенкмпвинтравлктабле**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | Указывает, какую таблицу с кодировкой переменной длины (Влк) следует использовать для написания кода энтропии.                             |
| [**еавенкмпвлевел**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | Задает профиль MPEG-2.                                                                             |
| [**еавенкмпвпрофиле**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | Задает профиль MPEG-2.                                                                             |
| [**еавенкмпвкскалетипе**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | Указывает, является ли шкала куантизер линейной или не линейной.                                            |
| [**еавенкмпвсканпаттерн**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | Указывает шаблон сканирования макроблокк.                                                                    |
| [**еавенкмпвсценедетектион**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | Указывает, как кодировщик ведет себя при обнаружении новой сцены.                                            |
| [**еавенкмуксаутпут**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | Указывает тип выходного потока, созданного мультиплексором.                                            |
| [**еавенквидеочромаресолутион**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | Указывает разрешение чрома.                                                                              |
| [**еавенквидеочромасубсамплинг**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | Указывает чрома заблокировано.                                                                                  |
| [**еавенквидеоколорлигхтинг**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | Указывает предполагаемые условия освещения для просмотра источника видео.                                    |
| [**еавенквидеоколорноминалранже**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | Указывает Номинальный диапазон для источника видео.                                                           |
| [**еавенквидеоколорпримариес**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | Задает цветовые цвета для видео.                                                               |
| [**еавенквидеоколортрансферфунктион**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | Указывает функцию преобразования из Р'Г'Б в RGB.                                                     |
| [**еавенквидеоколортрансферматрикс**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | Задает матрицу преобразования из цветового пространства И'кб'кр в цветовую область Р'Г'Б.                  |
| [**еавенквидеофилмконтент**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | Указывает, была ли первоначальным источником входного видео пленка или видео.                               |
| [**еавенквидеуутпутфрамератеконверсион**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | Указывает, преобразует ли кодировщик частоту кадров.                                                    |
| [**еавенквидеуутпутскантипе**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | Указывает, как кодировщик переводит выходное видео.                                                    |
| [**еавенквидеосаурцескантипе**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | Указывает, являются ли входные кадры кодировщика прогрессивными или чередуются.                          |
| [**еавфастдекодемоде**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | Указывает скорость декодирования видео.                                                                       |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по API кодека](codec-api-reference.md)
</dt> <dt>

[**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
