---
title: Справочник по видеозаписи
description: Справочник по видеозаписи
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Видео для Windows (VFW), Справочник по видеороликам
- VFW (видео для Windows), Справочник по видеороликам
- Авикап, Справочник
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067572"
---
# <a name="video-capture-reference"></a><span data-ttu-id="cee03-106">Справочник по видеозаписи</span><span class="sxs-lookup"><span data-stu-id="cee03-106">Video Capture Reference</span></span>

<span data-ttu-id="cee03-107">В этом разделе описываются функции, структуры, сообщения и макросы, связанные с классом окна Авикап.</span><span class="sxs-lookup"><span data-stu-id="cee03-107">This section describes the functions, structures, messages, and macros associated with the AVICap window class.</span></span> <span data-ttu-id="cee03-108">Эти элементы группируются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cee03-108">These elements are grouped as follows.</span></span>

## <a name="basic-capture-operations"></a><span data-ttu-id="cee03-109">Базовые операции записи</span><span class="sxs-lookup"><span data-stu-id="cee03-109">Basic Capture Operations</span></span>

-   [<span data-ttu-id="cee03-110">**капкреатекаптуревиндов**</span><span class="sxs-lookup"><span data-stu-id="cee03-110">**capCreateCaptureWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [<span data-ttu-id="cee03-111">**\_ \_ прекращение крепления WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-111">**WM\_CAP\_ABORT**</span></span>](wm-cap-abort.md)
-   [<span data-ttu-id="cee03-112">**\_ \_ Подключение к драйверу WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-112">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="cee03-113">**\_последовательность закрепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-113">**WM\_CAP\_SEQUENCE**</span></span>](wm-cap-sequence.md)
-   [<span data-ttu-id="cee03-114">**\_ \_ Окончание крепления WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-114">**WM\_CAP\_STOP**</span></span>](wm-cap-stop.md)

## <a name="capture-windows"></a><span data-ttu-id="cee03-115">Окна захвата</span><span class="sxs-lookup"><span data-stu-id="cee03-115">Capture Windows</span></span>

-   [<span data-ttu-id="cee03-116">**капстатус**</span><span class="sxs-lookup"><span data-stu-id="cee03-116">**CAPSTATUS**</span></span>](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [<span data-ttu-id="cee03-117">**капжетдривердескриптион**</span><span class="sxs-lookup"><span data-stu-id="cee03-117">**capGetDriverDescription**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [<span data-ttu-id="cee03-118">**\_ \_ Подключение к драйверу WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-118">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="cee03-119">**\_ \_ Отключение драйвера WM \_ Cap**</span><span class="sxs-lookup"><span data-stu-id="cee03-119">**WM\_CAP\_DRIVER\_DISCONNECT**</span></span>](wm-cap-driver-disconnect.md)
-   [<span data-ttu-id="cee03-120">**\_ \_ Получение состояния крепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-120">**WM\_CAP\_GET\_STATUS**</span></span>](wm-cap-get-status.md)

## <a name="capture-drivers"></a><span data-ttu-id="cee03-121">Драйверы записи</span><span class="sxs-lookup"><span data-stu-id="cee03-121">Capture Drivers</span></span>

-   [<span data-ttu-id="cee03-122">**капдриверкапс**</span><span class="sxs-lookup"><span data-stu-id="cee03-122">**CAPDRIVERCAPS**</span></span>](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [<span data-ttu-id="cee03-123">**\_драйвер крепления WM — \_ \_ Получение \_ политик авторизации подключений**</span><span class="sxs-lookup"><span data-stu-id="cee03-123">**WM\_CAP\_DRIVER\_GET\_CAPS**</span></span>](wm-cap-driver-get-caps.md)
-   [<span data-ttu-id="cee03-124">**\_ \_ \_ Получение \_ имени драйвера WM Cap**</span><span class="sxs-lookup"><span data-stu-id="cee03-124">**WM\_CAP\_DRIVER\_GET\_NAME**</span></span>](wm-cap-driver-get-name.md)
-   [<span data-ttu-id="cee03-125">**\_ \_ \_ Получение \_ версии драйвера WM Cap**</span><span class="sxs-lookup"><span data-stu-id="cee03-125">**WM\_CAP\_DRIVER\_GET\_VERSION**</span></span>](wm-cap-driver-get-version.md)
-   [<span data-ttu-id="cee03-126">**\_Получение закрепления WM \_ \_ аудиоформат**</span><span class="sxs-lookup"><span data-stu-id="cee03-126">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="cee03-127">**\_Получение закрепления WM \_ \_ видеоформат**</span><span class="sxs-lookup"><span data-stu-id="cee03-127">**WM\_CAP\_GET\_VIDEOFORMAT**</span></span>](wm-cap-get-videoformat.md)
-   [<span data-ttu-id="cee03-128">**\_Установка крепления \_ WM \_ аудиоформат**</span><span class="sxs-lookup"><span data-stu-id="cee03-128">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)
-   [<span data-ttu-id="cee03-129">**\_Установка крепления \_ WM \_ видеоформат**</span><span class="sxs-lookup"><span data-stu-id="cee03-129">**WM\_CAP\_SET\_VIDEOFORMAT**</span></span>](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a><span data-ttu-id="cee03-130">Предварительный просмотр и режимы наложения драйверов</span><span class="sxs-lookup"><span data-stu-id="cee03-130">Capture Driver Preview and Overlay Modes</span></span>

-   [<span data-ttu-id="cee03-131">**закрепление WM \_ \_ Set \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-131">**WM\_CAP\_SET\_OVERLAY**</span></span>](wm-cap-set-overlay.md)
-   [<span data-ttu-id="cee03-132">**\_ \_ \_ Предварительная версия WM Cap Set**</span><span class="sxs-lookup"><span data-stu-id="cee03-132">**WM\_CAP\_SET\_PREVIEW**</span></span>](wm-cap-set-preview.md)
-   [<span data-ttu-id="cee03-133">**\_Установка крепления \_ WM \_ превиеврате**</span><span class="sxs-lookup"><span data-stu-id="cee03-133">**WM\_CAP\_SET\_PREVIEWRATE**</span></span>](wm-cap-set-previewrate.md)
-   [<span data-ttu-id="cee03-134">**\_ \_ установленный масштаб WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-134">**WM\_CAP\_SET\_SCALE**</span></span>](wm-cap-set-scale.md)
-   [<span data-ttu-id="cee03-135">**закрепление WM \_ \_ Set \_ Scroll**</span><span class="sxs-lookup"><span data-stu-id="cee03-135">**WM\_CAP\_SET\_SCROLL**</span></span>](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a><span data-ttu-id="cee03-136">Диалоговые окна для захвата драйвера</span><span class="sxs-lookup"><span data-stu-id="cee03-136">Capture Driver Video Dialog Boxes</span></span>

-   [<span data-ttu-id="cee03-137">**\_видеокомпрессион с закреплениями WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-137">**WM\_CAP\_DLG\_VIDEOCOMPRESSION**</span></span>](wm-cap-dlg-videocompression.md)
-   [<span data-ttu-id="cee03-138">**\_видеодисплай с закреплениями WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-138">**WM\_CAP\_DLG\_VIDEODISPLAY**</span></span>](wm-cap-dlg-videodisplay.md)
-   [<span data-ttu-id="cee03-139">**\_видеоформат с закреплениями WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-139">**WM\_CAP\_DLG\_VIDEOFORMAT**</span></span>](wm-cap-dlg-videoformat.md)
-   [<span data-ttu-id="cee03-140">**\_видеосаурце с закреплениями WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-140">**WM\_CAP\_DLG\_VIDEOSOURCE**</span></span>](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a><span data-ttu-id="cee03-141">Формат аудио</span><span class="sxs-lookup"><span data-stu-id="cee03-141">Audio Format</span></span>

-   [<span data-ttu-id="cee03-142">**\_Получение закрепления WM \_ \_ аудиоформат**</span><span class="sxs-lookup"><span data-stu-id="cee03-142">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="cee03-143">**\_Установка крепления \_ WM \_ аудиоформат**</span><span class="sxs-lookup"><span data-stu-id="cee03-143">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a><span data-ttu-id="cee03-144">Параметры видеозаписи</span><span class="sxs-lookup"><span data-stu-id="cee03-144">Video Capture Settings</span></span>

-   [<span data-ttu-id="cee03-145">**каптурепармс**</span><span class="sxs-lookup"><span data-stu-id="cee03-145">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="cee03-146">**\_ \_ \_ Настройка последовательности получения крепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-146">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="cee03-147">**\_Установка закрепления WM \_ Set \_ Sequence \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-147">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a><span data-ttu-id="cee03-148">Запись файлов и буферов</span><span class="sxs-lookup"><span data-stu-id="cee03-148">Capture File and Buffers</span></span>

-   [<span data-ttu-id="cee03-149">**каптурепармс**</span><span class="sxs-lookup"><span data-stu-id="cee03-149">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="cee03-150">**\_выделение файла закрепления WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-150">**WM\_CAP\_FILE\_ALLOCATE**</span></span>](wm-cap-file-allocate.md)
-   [<span data-ttu-id="cee03-151">**файл \_ \_ \_ \_ записи получения закрепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-151">**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**</span></span>](wm-cap-file-get-capture-file.md)
-   [<span data-ttu-id="cee03-152">**\_закрепление \_ файла WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-152">**WM\_CAP\_FILE\_SAVEAS**</span></span>](wm-cap-file-saveas.md)
-   [<span data-ttu-id="cee03-153">**\_ \_ \_ \_ файл записи набора закрепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-153">**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**</span></span>](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a><span data-ttu-id="cee03-154">Непосредственное использование данных захвата</span><span class="sxs-lookup"><span data-stu-id="cee03-154">Directly Using Capture Data</span></span>

-   [<span data-ttu-id="cee03-155">**\_файл последовательности закрепления WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-155">**WM\_CAP\_SEQUENCE\_NOFILE**</span></span>](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a><span data-ttu-id="cee03-156">Захват с устройства MCI</span><span class="sxs-lookup"><span data-stu-id="cee03-156">Capture from MCI Device</span></span>

-   [<span data-ttu-id="cee03-157">**\_ \_ Установка \_ Устройства MCI с ЗАкреплениями WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-157">**WM\_CAP\_SET\_MCI\_DEVICE**</span></span>](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a><span data-ttu-id="cee03-158">Ручная запись кадров</span><span class="sxs-lookup"><span data-stu-id="cee03-158">Manual Frame Capture</span></span>

-   [<span data-ttu-id="cee03-159">**\_ \_ один кадр крепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-159">**WM\_CAP\_SINGLE\_FRAME**</span></span>](wm-cap-single-frame.md)
-   [<span data-ttu-id="cee03-160">**\_ \_ закрытие одиночного \_ кадра WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-160">**WM\_CAP\_SINGLE\_FRAME\_CLOSE**</span></span>](wm-cap-single-frame-close.md)
-   [<span data-ttu-id="cee03-161">**\_ \_ Открытие одиночного \_ кадра WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-161">**WM\_CAP\_SINGLE\_FRAME\_OPEN**</span></span>](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a><span data-ttu-id="cee03-162">Запись Still-Image</span><span class="sxs-lookup"><span data-stu-id="cee03-162">Still-Image Capture</span></span>

-   [<span data-ttu-id="cee03-163">**\_ \_ изменение копии крепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-163">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="cee03-164">**\_ \_ Файловый саведиб WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-164">**WM\_CAP\_FILE\_SAVEDIB**</span></span>](wm-cap-file-savedib.md)
-   [<span data-ttu-id="cee03-165">**\_ \_ блок захвата крепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-165">**WM\_CAP\_GRAB\_FRAME**</span></span>](wm-cap-grab-frame.md)
-   [<span data-ttu-id="cee03-166">**\_НЕостанавливаться \_ в \_ кадре захвата WM Cap \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-166">**WM\_CAP\_GRAB\_FRAME\_NOSTOP**</span></span>](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a><span data-ttu-id="cee03-167">Дополнительные параметры записи</span><span class="sxs-lookup"><span data-stu-id="cee03-167">Advanced Capture Options</span></span>

-   [<span data-ttu-id="cee03-168">**\_ \_ \_ инфочунк Установка файла закрепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-168">**WM\_CAP\_FILE\_SET\_INFOCHUNK**</span></span>](wm-cap-file-set-infochunk.md)
-   [<span data-ttu-id="cee03-169">**закрепление WM \_ \_ Получение \_ пользовательских \_ данных**</span><span class="sxs-lookup"><span data-stu-id="cee03-169">**WM\_CAP\_GET\_USER\_DATA**</span></span>](wm-cap-get-user-data.md)
-   [<span data-ttu-id="cee03-170">**закрепление WM \_ \_ Set \_ user \_ Data**</span><span class="sxs-lookup"><span data-stu-id="cee03-170">**WM\_CAP\_SET\_USER\_DATA**</span></span>](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a><span data-ttu-id="cee03-171">Работа с палитрами</span><span class="sxs-lookup"><span data-stu-id="cee03-171">Working with Palettes</span></span>

-   [<span data-ttu-id="cee03-172">**\_ \_ изменение копии крепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-172">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="cee03-173">**Автосоздание с \_ закреплениями WM Cap \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-173">**WM\_CAP\_PAL\_AUTOCREATE**</span></span>](wm-cap-pal-autocreate.md)
-   [<span data-ttu-id="cee03-174">**\_ \_ мануалкреатеи WM Cap PAL \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-174">**WM\_CAP\_PAL\_MANUALCREATE**</span></span>](wm-cap-pal-manualcreate.md)
-   [<span data-ttu-id="cee03-175">**\_ \_ открыт список доступа к КРЕПЛЕНИЯм WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-175">**WM\_CAP\_PAL\_OPEN**</span></span>](wm-cap-pal-open.md)
-   [<span data-ttu-id="cee03-176">**\_Вставка крепления WM \_ PAL \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-176">**WM\_CAP\_PAL\_PASTE**</span></span>](wm-cap-pal-paste.md)
-   [<span data-ttu-id="cee03-177">**\_Сохранение крепления WM \_ PAL \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-177">**WM\_CAP\_PAL\_SAVE**</span></span>](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a><span data-ttu-id="cee03-178">Передается другим приложениям</span><span class="sxs-lookup"><span data-stu-id="cee03-178">Yielding to Other Applications</span></span>

-   [<span data-ttu-id="cee03-179">**\_ \_ \_ Настройка последовательности получения крепления \_ WM**</span><span class="sxs-lookup"><span data-stu-id="cee03-179">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="cee03-180">**\_ \_ \_ вызов функции обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-180">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="cee03-181">**\_Установка закрепления WM \_ Set \_ Sequence \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-181">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a><span data-ttu-id="cee03-182">Функции обратного вызова Авикап</span><span class="sxs-lookup"><span data-stu-id="cee03-182">AVICap Callback Functions</span></span>

-   [<span data-ttu-id="cee03-183">**капконтролкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cee03-183">**capControlCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [<span data-ttu-id="cee03-184">**каперроркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cee03-184">**capErrorCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [<span data-ttu-id="cee03-185">**капстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cee03-185">**capStatusCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [<span data-ttu-id="cee03-186">**капвидеостреамкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cee03-186">**capVideoStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [<span data-ttu-id="cee03-187">**капвавестреамкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cee03-187">**capWaveStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [<span data-ttu-id="cee03-188">**капиелдкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cee03-188">**capYieldCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [<span data-ttu-id="cee03-189">**\_ \_ \_ капконтрол обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-189">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)
-   [<span data-ttu-id="cee03-190">**\_ \_ \_ ошибка обратного вызова установки крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-190">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="cee03-191">**\_ \_ \_ кадр обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-191">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)
-   [<span data-ttu-id="cee03-192">**\_ \_ \_ состояние обратного вызова Set Cap WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-192">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="cee03-193">**\_ \_ \_ VIDEOSTREAM обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-193">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="cee03-194">**\_ \_ \_ вавестреам обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-194">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)
-   [<span data-ttu-id="cee03-195">**\_ \_ \_ вызов функции обратного вызова Set крепления WM \_**</span><span class="sxs-lookup"><span data-stu-id="cee03-195">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a><span data-ttu-id="cee03-196">См. также</span><span class="sxs-lookup"><span data-stu-id="cee03-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee03-197">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="cee03-197">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 




