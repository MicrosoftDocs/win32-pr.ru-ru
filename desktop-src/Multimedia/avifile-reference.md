---
title: Справочник по Авифиле
description: Справочник по Авифиле
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b4bbda5374f5b1418c166aae5efcc06168b522b2cae0f3b6d2c8fe3c069c36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808324"
---
# <a name="avifile-reference"></a>Справочник по Авифиле

В этом разделе описываются функции, структуры и макросы для приложений, использующих службы Авифиле Services. Эти элементы группируются следующим образом:

## <a name="avifile-library-operations"></a>Операции с библиотекой Авифиле

-   [**авифилеинит**](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [**авифиликсит**](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a>Открытие и закрытие AVI файлов

-   [**авифилеопен**](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [**авифилеаддреф**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [**авифилерелеасе**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [**жетопенфиленамепревиев**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a>Чтение из файла

-   [**авифилеинфо**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [**авифилеинфо**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [**авифилереаддата**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a>Запись в файл

-   [**авифилевритедата**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a>Использование буфера обмена

-   [**авипутфилеонклипбоард**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [**авижетфромклипбоард**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [**авиклеарклипбоард**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a>открытие и закрытие Потоки

-   [**авифилежетстреам**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [**авистреамопенфромфиле**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [**авистреамаддреф**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [**авистреамрелеасе**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a>Чтение сведений о потоке

-   [**авистреаминфо**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [**авистреамреаддата**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [**авистреамдатасизе**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [**авистреамреадформат**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [**авистреамформатсизе**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [**авистреамреад**](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [**авистреамсамплесизе**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [**авистреамбегинстреаминг**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [**авистреамендстреаминг**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a>Распаковка данных видео в потоке

-   [**авистреамжетфрамеопен**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [**авистреамжетфраме**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [**авистреамжетфрамеклосе**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a>создание файла из существующего Потоки

-   [**ависаве**](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [**ависавев**](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [**ависавеоптионс**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [**жетсавефиленамепревиев**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [**авимакефилефромстреамс**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a>запись отдельных Потоки

-   [**авифилекреатестреам**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [**авистреамсетформат**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [**авистреамврите**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [**авифилевритедата**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [**авистреамвритедата**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [**авистреамрелеасе**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a>Поиск начальной положения в потоке

-   [**авистреамстарт**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [**авистреамстарттиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [**авистреамленгс**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [**авистреамленгстиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [**авистреамфиндсампле**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**авистреаменд**](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [**авистреамендтиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a>Поиск образца и ключевых кадров

-   [**авистреамфиндсампле**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**авистреамискэйфраме**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [**авистреамнеаресткэйфраме**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [**авистреамнеаресткэйфраметиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [**авистреамнеарестсампле**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [**авистреамнеарестсамплетиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [**авистреамнексткэйфраме**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [**авистреамнексткэйфраметиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [**авистреамнекстсампле**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [**авистреамнекстсамплетиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [**авистреампревкэйфраме**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [**авистреампревкэйфраметиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [**авистреампревсампле**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [**авистреампревсамплетиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [**авистреамсамплетосампле**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a>Переключение между образцами и временем

-   [**авистреамсамплетотиме**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [**авистреамтиметосампле**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a>создание временных Потоки

-   [**авистреамкреате**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [**авимакекомпресседстреам**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [**авистреамрелеасе**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a>редактирование Потоки AVI

-   [**креатидитаблестреам**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [**едитстреамкут**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [**едитстреамкопи**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [**едитстреампасте**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [**едитстреамклоне**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [**едитстреамсетинфо**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [**едитстреамсетнаме**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции и макросы Авифиле](avifile-functions-and-macros.md)
</dt> </dl>

 

 




