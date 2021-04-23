---
title: Запись мультимедиа
description: Запись мультимедиа
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- Функция МЦивндкреате
- Макрос МЦивнднев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410917"
---
# <a name="multimedia-recording"></a><span data-ttu-id="0441e-105">Запись мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0441e-105">Multimedia Recording</span></span>

<span data-ttu-id="0441e-106">Вы можете реализовать возможности записи в приложении с помощью пользовательского интерфейса, встроенного в МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="0441e-106">You can implement recording capabilities in your application by using the user interface built into MCIWnd.</span></span> <span data-ttu-id="0441e-107">Вы можете использовать функцию [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) и макрос [**мЦивнднев**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) для предоставления элементов управления для запуска и остановки записи и для сохранения записанных данных.</span><span class="sxs-lookup"><span data-stu-id="0441e-107">You can use the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to provide controls for starting and stopping recording and for saving the recorded information.</span></span> <span data-ttu-id="0441e-108">С помощью **мЦивндкреате** можно указать стили окна для вывода окна мЦивнд и включения кнопки **запись** на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="0441e-108">Using **MCIWndCreate**, you can specify window styles to display an MCIWnd window and to include the **Record** button on the toolbar.</span></span> <span data-ttu-id="0441e-109">С помощью **мЦивнднев** можно указать записываемый тип устройства и указать, что данные должны быть записаны в новый файл.</span><span class="sxs-lookup"><span data-stu-id="0441e-109">Using **MCIWndNew**, you can specify the device type that is being recorded and specify that the information is to be captured in a new file.</span></span>

<span data-ttu-id="0441e-110">Если приложению требуется более изощренная Настройка, можно автоматизировать и настроить запись с помощью макроса [**мЦивндрекорд**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) .</span><span class="sxs-lookup"><span data-stu-id="0441e-110">If your application requires more sophistication, you can automate and customize the recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="0441e-111">Дополнительные сведения см. [в разделе Настройка процесса записи](customizing-the-recording-process.md).</span><span class="sxs-lookup"><span data-stu-id="0441e-111">For more information, see [Customizing the Recording Process](customizing-the-recording-process.md).</span></span>

> [!Note]  
> <span data-ttu-id="0441e-112">Некоторые устройства, такие как CD Audio и МЦИАВИ, используются только для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0441e-112">Some devices, such as CD audio and MCIAVI, are used for playback only.</span></span> <span data-ttu-id="0441e-113">Для записи можно использовать другие устройства, например устройства аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="0441e-113">Other devices, such as waveform-audio devices, can be used for recording.</span></span> <span data-ttu-id="0441e-114">Если указать устройство, которое не может записать, МЦивнд пропускает кнопку **записи** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="0441e-114">If you specify a device that cannot record, MCIWnd omits the **Record** button from the toolbar.</span></span>

 

 

 




