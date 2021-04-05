---
title: Режимы просмотра и наложения
description: Режимы просмотра и наложения
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- Сообщение WM_CAP_SET_PREVIEW
- макрос Каппревиев
- Сообщение WM_CAP_SET_PREVIEWRATE
- макрос Каппревиеврате
- Сообщение WM_CAP_SET_SCALE
- макрос Каппревиевскале
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986363"
---
# <a name="preview-and-overlay-modes"></a><span data-ttu-id="9fa71-109">Режимы просмотра и наложения</span><span class="sxs-lookup"><span data-stu-id="9fa71-109">Preview and Overlay Modes</span></span>

<span data-ttu-id="9fa71-110">Драйвер записи может реализовать два метода просмотра входящего видеопотока: режим предварительного просмотра и режим наложения.</span><span class="sxs-lookup"><span data-stu-id="9fa71-110">A capture driver can implement two methods for viewing an incoming video stream: preview mode and overlay mode.</span></span> <span data-ttu-id="9fa71-111">Если драйвер записи реализует оба метода, пользователь может выбрать используемый метод.</span><span class="sxs-lookup"><span data-stu-id="9fa71-111">If a capture driver implements both methods, the user can choose which method to use.</span></span>

<span data-ttu-id="9fa71-112">Режим предварительного просмотра передает оцифрованные кадры от оборудования захвата в память системы, а затем отображает оцифрованные кадры в окне Capture с помощью функций интерфейса графических устройств (GDI).</span><span class="sxs-lookup"><span data-stu-id="9fa71-112">Preview mode transfers digitized frames from the capture hardware to system memory and then displays the digitized frames in the capture window by using graphics device interface (GDI) functions.</span></span> <span data-ttu-id="9fa71-113">Приложения могут уменьшить скорость предварительной версии, когда родительское окно теряет фокус, и увеличивать скорость предварительного просмотра, когда родительское окно получает фокус.</span><span class="sxs-lookup"><span data-stu-id="9fa71-113">Applications might decrease the preview rate when the parent window loses focus, and increase the preview rate when the parent window gains focus.</span></span> <span data-ttu-id="9fa71-114">Это действие повышает скорость реагирования системы, поскольку операция предварительной версии требует интенсивного функционирования процессора.</span><span class="sxs-lookup"><span data-stu-id="9fa71-114">This action improves general system responsiveness because the preview operation is processor intensive.</span></span>

<span data-ttu-id="9fa71-115">Существует три сообщения для управления операцией просмотра.</span><span class="sxs-lookup"><span data-stu-id="9fa71-115">There are three messages to control the preview operation.</span></span>

-   <span data-ttu-id="9fa71-116">Чтобы включить или отключить режим предварительного просмотра, используйте сообщение с [**\_ закреплениями WM \_ Set \_**](wm-cap-set-preview.md) , отправив (или макрос [**каппревиев**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="9fa71-116">Use the [**WM\_CAP\_SET\_PREVIEW**](wm-cap-set-preview.md) message to enable or disable preview mode by sending the (or the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro) to a capture window.</span></span>
-   <span data-ttu-id="9fa71-117">Используйте сообщение [**WM \_ Cap \_ Set \_ Превиеврате**](wm-cap-set-previewrate.md) (или макрос [**каппревиеврате**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ), чтобы задать скорость отображения кадров в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="9fa71-117">Use the [**WM\_CAP\_SET\_PREVIEWRATE**](wm-cap-set-previewrate.md) message (or the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro) to set the rate at which frames are displayed in preview mode</span></span>
-   <span data-ttu-id="9fa71-118">Чтобы включить или отключить масштабирование видео в режиме предварительного просмотра, используйте сообщение с [**\_ закреплениями WM \_ Set \_ Scale**](wm-cap-set-scale.md) (или макрос [**каппревиевскале**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ).</span><span class="sxs-lookup"><span data-stu-id="9fa71-118">Use the [**WM\_CAP\_SET\_SCALE**](wm-cap-set-scale.md) message (or the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro) to enable or disable scaling of the preview video.</span></span>

<span data-ttu-id="9fa71-119">Если предварительный просмотр и масштабирование включены, записанный видеокадр растягивается по размерам окна Capture.</span><span class="sxs-lookup"><span data-stu-id="9fa71-119">When preview and scaling are both enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="9fa71-120">Включение режима предварительного просмотра автоматически отключает режим наложения.</span><span class="sxs-lookup"><span data-stu-id="9fa71-120">Enabling preview mode automatically disables overlay mode.</span></span>

<span data-ttu-id="9fa71-121">Режим наложения — это аппаратная функция, которая отображает содержимое буфера записи на мониторе без использования ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="9fa71-121">Overlay mode is a hardware function that displays the contents of the capture buffer on the monitor without using CPU resources.</span></span> <span data-ttu-id="9fa71-122">Вы можете включить и отключить режим наложения, отправив сообщение о [**\_ \_ \_ наложении закрепления WM**](wm-cap-set-overlay.md) (или макрос [**каповерлай**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="9fa71-122">You can enable and disable overlay mode by sending the [**WM\_CAP\_SET\_OVERLAY**](wm-cap-set-overlay.md) message (or the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro) to a capture window.</span></span> <span data-ttu-id="9fa71-123">Включение режима наложения автоматически отключает режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="9fa71-123">Enabling overlay mode automatically disables preview mode.</span></span>

<span data-ttu-id="9fa71-124">Вы также можете задать расположение прокрутки видеокадра в клиентской области окна записи для режима предварительного просмотра или режима наложения, отправив сообщение с [**\_ \_ \_ прокруткой WM Cap Set**](wm-cap-set-scroll.md) (или макрос [**капсетскроллпос**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="9fa71-124">You can also set the scroll position of the video frame within the client area of the capture window for preview mode or overlay mode by sending the [**WM\_CAP\_SET\_SCROLL**](wm-cap-set-scroll.md) message (or the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro) to a capture window.</span></span>

 

 




