---
title: Состояние окна записи
description: Состояние окна записи
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- Сообщение WM_CAP_GET_STATUS
- макрос Капжетстатус
- Структура КАПСТАТУС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068368"
---
# <a name="capture-window-status"></a><span data-ttu-id="cb6f1-106">Состояние окна записи</span><span class="sxs-lookup"><span data-stu-id="cb6f1-106">Capture Window Status</span></span>

<span data-ttu-id="cb6f1-107">Вы можете получить текущее состояние окна записи, используя сообщение [**\_ \_ \_ о состоянии с закреплениями WM**](wm-cap-get-status.md) (или макрос [**капжетстатус**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ).</span><span class="sxs-lookup"><span data-stu-id="cb6f1-107">You can retrieve the current status of a capture window by using the [**WM\_CAP\_GET\_STATUS**](wm-cap-get-status.md) message (or the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro).</span></span> <span data-ttu-id="cb6f1-108">Это сообщение извлекает копию структуры [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) с текущими значениями ее элементов.</span><span class="sxs-lookup"><span data-stu-id="cb6f1-108">This message retrieves a copy of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure with the current values of its members.</span></span> <span data-ttu-id="cb6f1-109">Структура **капстатус** содержит сведения об измерениях изображения, положении прокрутки и о том, включено ли наложение или предварительный просмотр изображения.</span><span class="sxs-lookup"><span data-stu-id="cb6f1-109">The **CAPSTATUS** structure contains information regarding the dimensions of the image, scroll position, and whether overlay or preview of the image is enabled.</span></span> <span data-ttu-id="cb6f1-110">Так как сведения, представленные в **капстатус** , являются динамическими, приложение должно обновлять содержимое структуры каждый раз, когда размер или формат захваченного видеопотока может измениться (например, после отображения видеоформата драйвера записи).</span><span class="sxs-lookup"><span data-stu-id="cb6f1-110">Because the information represented in **CAPSTATUS** is dynamic, your application should refresh the contents of the structure whenever the size or format of the captured video stream might have changed (such as after displaying the video format of the capture driver).</span></span>

<span data-ttu-id="cb6f1-111">Изменение размеров окна захвата не влияет на размеры потока записанного видео.</span><span class="sxs-lookup"><span data-stu-id="cb6f1-111">Changing the dimensions of the capture window has no effect on the dimensions of the actual captured video stream.</span></span> <span data-ttu-id="cb6f1-112">Диалоговое окно Формат, отображаемое драйвером устройства записи видео, управляет размерами записанного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="cb6f1-112">The format dialog box displayed by the video capture device driver controls the dimensions of the captured video stream.</span></span>

 

 




