---
description: Команды DVD
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: Команды DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02f9c0b6a50b6d7eb67832286ee980b0faf69460621a46caf98089efc24b19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820588"
---
# <a name="dvd-commands"></a>Команды DVD

команды навигации и воспроизведения dvd-диска определены в разделе, посвященном спецификации dvd с именем приложение j, поэтому DirectShowная документация часто относится к "командам в приложении j". имена, заданные в приложении J, не всегда очень интуитивно понятны, поэтому DirectShow использует имена, которые могут быть проще в понимании.

в следующей таблице перечислены команды в приложении J и их DirectShow эквиваленты.



| Команда в приложении J                                                                           | Описание                                                                  | Метод IDvdControl2                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| \_Воспроизвести название                                                                               | Воспроизвести заголовок.                                                                | [**плайтитле**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PTT \_ Play                                                                                 | Воспроизводить главу в заголовке.                                                   | [**плайчаптеринтитле**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| \_Воспроизведение времени                                                                                | Воспроизвести заголовок, начиная с указанного времени.                                 | [**плайаттимеинтитле**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Stop                                                                                      | Останавливает воспроизведение.                                                               | [**Позиции**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| Группы                                                                                      | Возврат из подменю в родительское меню.                                    | [**ретурнфромсубмену**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| Поиск по времени \_                                                                              | Воспроизвести в указанное время в текущем заголовке.                           | [**плайаттиме**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| \_Поиск PTT                                                                               | Воспроизвести главу в текущем заголовке.                                     | [**плайчаптер**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| \_Поиск превпг                                                                            | Перейдите к началу предыдущей главы и возобновите воспроизведение.                 | [**плайпревчаптер**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| \_Поиск топпг                                                                             | Перейти к началу текущей главы и возобновить воспроизведение.                  | [**реплайчаптер**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| \_Поиск некстпг                                                                            | Перейдите к началу следующей главы и возобновите воспроизведение.                     | [**плайнекстчаптер**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Прямая \_ Проверка                                                                             | Воспроизведение вперед с указанной скоростью воспроизведения. Скорость воспроизведения по умолчанию — 1,0. | [**плайфорвардс**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| Обратная \_ Проверка                                                                            | Воспроизведение назад с указанным темпом воспроизведения.                                  | [**плайбакквардс**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| \_Вызов меню                                                                                | показать меню;                                                                 | [**шовмену**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Возобновить                                                                                    | Возврат из меню и возобновление воспроизведения.                                      | [**Возобновить**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| \_Кнопка "вверх" (нажатие кнопки \_ ), кнопка "вниз" (нажатие кнопки) \_ \_ , стрелка влево \_ \_ \_ \_ , выбор | Выберите кнопку, положенную относительно выбранной в данный момент кнопки. | [**селектбуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Кнопка " \_ Активировать"                                                                          | Активировать выбранную кнопку.                                                | [**активатебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| Кнопка " \_ выбрать \_ и \_ Активировать"                                                             | Выберите и активируйте кнопку.                                                | [**селектандактиватебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| По-прежнему \_ отключено                                                                                | Возобновить воспроизведение при отображении изображения по-прежнему.                               | [**стиллофф**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Пауза \_ вкл.                                                                                 | Приостановить воспроизведение.                                                              | [**Пауза**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Приостановить \_                                                                                | Возобновить воспроизведение в приостановленном состоянии.                                       | [**Пауза**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| \_Выбор языка \_ меню                                                                    | Выберите язык для меню.                                               | [**селектдефаултменулангуаже**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| \_Изменение аудиопотока \_                                                                     | Задайте аудиопоток.                                                        | [**селектаудиостреам**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Изменение потока вспомогательных рисунков \_ \_                                                               | Задание потока субтитров; включить или отключить отображение субтитров.             | [**селектсубпиктурестреам**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| \_Изменение угла                                                                             | Задайте угол камеры.                                                        | [**селектангле**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| \_Выбор родительского уровня \_                                                                   | Задайте родительский уровень.                                                      | [**селектпаренталлевел**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| Родительский \_ \_ Выбор страны                                                                 | Задайте страну или регион для родительского управления.                              | [**селектпаренталкаунтри**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| \_ \_ \_ Изменение режима звуковой презентации \_ Караоке                                                | Установите режим смешения звука для караоке.                                       | [**селекткараокеаудиопресентатионмоде**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| \_ \_ Изменение режима видеопрезентации \_                                                         | Установите для режима пропорций значение широкоэкранный, леттербокс или панорамный просмотр.             | [**селектвидеомодепреференце**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> </dl>

 

 



