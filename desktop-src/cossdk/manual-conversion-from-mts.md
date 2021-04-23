---
description: Ручное преобразование из MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Ручное преобразование из MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807373"
---
# <a name="manual-conversion-from-mts"></a><span data-ttu-id="4fcde-103">Ручное преобразование из MTS</span><span class="sxs-lookup"><span data-stu-id="4fcde-103">Manual Conversion from MTS</span></span>

<span data-ttu-id="4fcde-104">Может потребоваться изолировать преобразование пакетов MTS в приложения COM+, чтобы оно находилось вне процесса установки Windows.</span><span class="sxs-lookup"><span data-stu-id="4fcde-104">You might want to isolate conversion of MTS packages to COM+ applications so that it is outside the Windows setup process.</span></span> <span data-ttu-id="4fcde-105">Следующая процедура предлагает альтернативный подход:</span><span class="sxs-lookup"><span data-stu-id="4fcde-105">The following procedure offers an alternate approach:</span></span>

1.  <span data-ttu-id="4fcde-106">Экспортируйте пакеты MTS с помощью функции экспорта пакетов MTS 2,0 (в результате чего файл пакета MTS и коллекция других файлов).</span><span class="sxs-lookup"><span data-stu-id="4fcde-106">Export the MTS packages using the MTS 2.0 Package Export feature (resulting in an MTS package file and a collection of other files).</span></span>
2.  <span data-ttu-id="4fcde-107">Удалите пакеты MTS и обновите Windows, либо выполните чистую установку Windows.</span><span class="sxs-lookup"><span data-stu-id="4fcde-107">Delete the MTS packages and upgrade Windows, or perform a clean installation of Windows.</span></span>
3.  <span data-ttu-id="4fcde-108">Установите файлы пакета MTS (. Pak) в системе Windows 2000 или более поздней версии с помощью мастера установки приложения "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="4fcde-108">Install the MTS package (.pak) files on a Windows 2000 or later system by using the Component Services administrative tool's Application Install wizard.</span></span> <span data-ttu-id="4fcde-109">Кроме того, необходимо сбросить удостоверение "Запуск от имени" приложения в системном реестре в разделе **hKey \_ Local \_ Machine \\ Software \\ Classes \\ AppID \\ runas**.</span><span class="sxs-lookup"><span data-stu-id="4fcde-109">You will also need to reset the application's "Run As" identity in the system registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\APPID\\RunAs**.</span></span>

> [!Note]  
> <span data-ttu-id="4fcde-110">Файл журнала МТСТОКОМ создается только процедурой автоматического преобразования (с помощью программы установки Windows или запуска служебной программы МТСТОКОМ).</span><span class="sxs-lookup"><span data-stu-id="4fcde-110">Only the automatic conversion procedure (through Windows setup or by running the MTSTOCOM utility) generates the MTSTOCOM log file.</span></span> <span data-ttu-id="4fcde-111">Этот файл не создается при выполнении процедуры преобразования вручную.</span><span class="sxs-lookup"><span data-stu-id="4fcde-111">This file is not generated when following the manual conversion procedure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4fcde-112">См. также</span><span class="sxs-lookup"><span data-stu-id="4fcde-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fcde-113">Автоматическое преобразование из MTS</span><span class="sxs-lookup"><span data-stu-id="4fcde-113">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="4fcde-114">Результаты и проблемы преобразования COM+</span><span class="sxs-lookup"><span data-stu-id="4fcde-114">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="4fcde-115">Библиотека администрирования MTS</span><span class="sxs-lookup"><span data-stu-id="4fcde-115">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



