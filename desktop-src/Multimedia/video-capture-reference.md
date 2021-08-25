---
title: Справочник по видеозаписи
description: Справочник по видеозаписи
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- видео для Windows (VFW), справочник по видеороликам
- VFW (видео для Windows), справочник по видеороликам
- Авикап, Справочник
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 166bdcf06e700023a197334b0e63f612398485affe21dc9ffbc6e7ac0800926a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804314"
---
# <a name="video-capture-reference"></a>Справочник по видеозаписи

В этом разделе описываются функции, структуры, сообщения и макросы, связанные с классом окна Авикап. Эти элементы группируются следующим образом.

## <a name="basic-capture-operations"></a>Базовые операции записи

-   [**капкреатекаптуревиндов**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**\_ \_ прекращение крепления WM**](wm-cap-abort.md)
-   [**\_ \_ Подключение к драйверу WM Cap \_**](wm-cap-driver-connect.md)
-   [**\_последовательность закрепления WM \_**](wm-cap-sequence.md)
-   [**\_ \_ Окончание крепления WM**](wm-cap-stop.md)

## <a name="capture-windows"></a>Windows записи

-   [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**капжетдривердескриптион**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**\_ \_ Подключение к драйверу WM Cap \_**](wm-cap-driver-connect.md)
-   [**\_ \_ Отключение драйвера WM \_ Cap**](wm-cap-driver-disconnect.md)
-   [**\_ \_ Получение состояния крепления \_ WM**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Драйверы записи

-   [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**\_драйвер крепления WM — \_ \_ Получение \_ политик авторизации подключений**](wm-cap-driver-get-caps.md)
-   [**\_ \_ \_ Получение \_ имени драйвера WM Cap**](wm-cap-driver-get-name.md)
-   [**\_ \_ \_ Получение \_ версии драйвера WM Cap**](wm-cap-driver-get-version.md)
-   [**\_Получение закрепления WM \_ \_ аудиоформат**](wm-cap-get-audioformat.md)
-   [**\_Получение закрепления WM \_ \_ видеоформат**](wm-cap-get-videoformat.md)
-   [**\_Установка крепления \_ WM \_ аудиоформат**](wm-cap-set-audioformat.md)
-   [**\_Установка крепления \_ WM \_ видеоформат**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Предварительный просмотр и режимы наложения драйверов

-   [**закрепление WM \_ \_ Set \_**](wm-cap-set-overlay.md)
-   [**\_ \_ \_ Предварительная версия WM Cap Set**](wm-cap-set-preview.md)
-   [**\_Установка крепления \_ WM \_ превиеврате**](wm-cap-set-previewrate.md)
-   [**\_ \_ установленный масштаб WM Cap \_**](wm-cap-set-scale.md)
-   [**закрепление WM \_ \_ Set \_ Scroll**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Диалоговые окна для захвата драйвера

-   [**\_видеокомпрессион с закреплениями WM \_ \_**](wm-cap-dlg-videocompression.md)
-   [**\_видеодисплай с закреплениями WM \_ \_**](wm-cap-dlg-videodisplay.md)
-   [**\_видеоформат с закреплениями WM \_ \_**](wm-cap-dlg-videoformat.md)
-   [**\_видеосаурце с закреплениями WM \_ \_**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Формат аудио

-   [**\_Получение закрепления WM \_ \_ аудиоформат**](wm-cap-get-audioformat.md)
-   [**\_Установка крепления \_ WM \_ аудиоформат**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Параметры видеозаписи

-   [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_ \_ \_ Настройка последовательности получения крепления \_ WM**](wm-cap-get-sequence-setup.md)
-   [**\_Установка закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Запись файлов и буферов

-   [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_выделение файла закрепления WM \_ \_**](wm-cap-file-allocate.md)
-   [**файл \_ \_ \_ \_ записи получения закрепления \_ WM**](wm-cap-file-get-capture-file.md)
-   [**\_закрепление \_ файла WM Cap \_**](wm-cap-file-saveas.md)
-   [**\_ \_ \_ \_ файл записи набора закрепления \_ WM**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Непосредственное использование данных захвата

-   [**\_файл последовательности закрепления WM \_ \_**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Захват с устройства MCI

-   [**\_ \_ Установка \_ Устройства MCI с ЗАкреплениями WM \_**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Ручная запись кадров

-   [**\_ \_ один кадр крепления \_ WM**](wm-cap-single-frame.md)
-   [**\_ \_ закрытие одиночного \_ кадра WM Cap \_**](wm-cap-single-frame-close.md)
-   [**\_ \_ Открытие одиночного \_ кадра WM Cap \_**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Запись Still-Image

-   [**\_ \_ изменение копии крепления \_ WM**](wm-cap-edit-copy.md)
-   [**\_ \_ Файловый саведиб WM Cap \_**](wm-cap-file-savedib.md)
-   [**\_ \_ блок захвата крепления \_ WM**](wm-cap-grab-frame.md)
-   [**\_НЕостанавливаться \_ в \_ кадре захвата WM Cap \_**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Дополнительные параметры записи

-   [**\_ \_ \_ инфочунк Установка файла закрепления WM \_**](wm-cap-file-set-infochunk.md)
-   [**закрепление WM \_ \_ Получение \_ пользовательских \_ данных**](wm-cap-get-user-data.md)
-   [**закрепление WM \_ \_ Set \_ user \_ Data**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Работа с палитрами

-   [**\_ \_ изменение копии крепления \_ WM**](wm-cap-edit-copy.md)
-   [**Автосоздание с \_ закреплениями WM Cap \_ \_**](wm-cap-pal-autocreate.md)
-   [**\_ \_ мануалкреатеи WM Cap PAL \_**](wm-cap-pal-manualcreate.md)
-   [**\_ \_ открыт список доступа к КРЕПЛЕНИЯм WM \_**](wm-cap-pal-open.md)
-   [**\_Вставка крепления WM \_ PAL \_**](wm-cap-pal-paste.md)
-   [**\_Сохранение крепления WM \_ PAL \_**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Передается другим приложениям

-   [**\_ \_ \_ Настройка последовательности получения крепления \_ WM**](wm-cap-get-sequence-setup.md)
-   [**\_ \_ \_ вызов функции обратного вызова Set крепления WM \_**](wm-cap-set-callback-yield.md)
-   [**\_Установка закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>Функции обратного вызова Авикап

-   [**капконтролкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**каперроркаллбакк**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**капстатускаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**капвидеостреамкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**капвавестреамкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**капиелдкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**\_ \_ \_ капконтрол обратного вызова Set крепления WM \_**](wm-cap-set-callback-capcontrol.md)
-   [**\_ \_ \_ ошибка обратного вызова установки крепления WM \_**](wm-cap-set-callback-error.md)
-   [**\_ \_ \_ кадр обратного вызова Set крепления WM \_**](wm-cap-set-callback-frame.md)
-   [**\_ \_ \_ состояние обратного вызова Set Cap WM \_**](wm-cap-set-callback-status.md)
-   [**\_ \_ \_ VIDEOSTREAM обратного вызова Set крепления WM \_**](wm-cap-set-callback-videostream.md)
-   [**\_ \_ \_ вавестреам обратного вызова Set крепления WM \_**](wm-cap-set-callback-wavestream.md)
-   [**\_ \_ \_ вызов функции обратного вызова Set крепления WM \_**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 




