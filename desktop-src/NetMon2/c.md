---
description: Глоссарий сетевой монитор терминов, начинающихся с буквы C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (сетевой монитор)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650775"
---
# <a name="c-network-monitor"></a><span data-ttu-id="aff9e-103">C (сетевой монитор)</span><span class="sxs-lookup"><span data-stu-id="aff9e-103">C (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="aff9e-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**выделяем**</span><span class="sxs-lookup"><span data-stu-id="aff9e-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**capture**</span></span>
</dt> <dd>

<span data-ttu-id="aff9e-105">Данные сетевого трафика, собираемые в кадрах.</span><span class="sxs-lookup"><span data-stu-id="aff9e-105">Network traffic data that is collected in frames.</span></span> <span data-ttu-id="aff9e-106">Поставщик сетевых пакетов (НПП) выполняет запись.</span><span class="sxs-lookup"><span data-stu-id="aff9e-106">A network packet provider (NPP) performs a capture.</span></span> <span data-ttu-id="aff9e-107">См. также [*Отложенная запись*](d.md)и *запись в реальном времени*</span><span class="sxs-lookup"><span data-stu-id="aff9e-107">See also [*delayed capture*](d.md), and *real-time capture*</span></span>

</dd> <dt>

<span data-ttu-id="aff9e-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**файл записи**</span><span class="sxs-lookup"><span data-stu-id="aff9e-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capture file**</span></span>
</dt> <dd>

<span data-ttu-id="aff9e-109">Файл, который сетевой монитор создает для хранения захваченных данных.</span><span class="sxs-lookup"><span data-stu-id="aff9e-109">A file that Network Monitor creates to store captured data.</span></span> <span data-ttu-id="aff9e-110">Расширение файла. Cap определяет файл записи.</span><span class="sxs-lookup"><span data-stu-id="aff9e-110">The .cap file name extension identifies a capture file.</span></span> <span data-ttu-id="aff9e-111">Сетевой монитор случайным образом создает имя файла записи, но имя файла можно изменить при сохранении файла записи.</span><span class="sxs-lookup"><span data-stu-id="aff9e-111">Network Monitor randomly generates a capture file name, but you can change the file name when you save the capture file.</span></span>

<span data-ttu-id="aff9e-112">Сетевой монитор создает файл записи каждый раз при запуске процесса записи, а затем сохраняет его во время процесса записи.</span><span class="sxs-lookup"><span data-stu-id="aff9e-112">Network Monitor creates a capture file each time the capture process starts, and then keeps the file open during the capture process.</span></span> <span data-ttu-id="aff9e-113">Доступ к содержимому файла записи невозможен, пока процесс записи не будет остановлен и файл записи не будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="aff9e-113">You cannot access the contents of a capture file until the capture process is stopped and the capture file is closed.</span></span>

</dd> <dt>

<span data-ttu-id="aff9e-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**фильтр записи**</span><span class="sxs-lookup"><span data-stu-id="aff9e-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**capture filter**</span></span>
</dt> <dd>

<span data-ttu-id="aff9e-115">Набор функций сетевой монитор, используемых для ограничения входящих кадров, используемых приложением поставщика сетевых пакетов (НПП).</span><span class="sxs-lookup"><span data-stu-id="aff9e-115">A set of Network Monitor functions used to restrict incoming frames that a network packet provider (NPP) application uses.</span></span>

</dd> <dt>

<span data-ttu-id="aff9e-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**триггер записи**</span><span class="sxs-lookup"><span data-stu-id="aff9e-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**capture trigger**</span></span>
</dt> <dd>

<span data-ttu-id="aff9e-117">Событие триггера, заданное для отмены процесса записи.</span><span class="sxs-lookup"><span data-stu-id="aff9e-117">A trigger event that is set to stop the capture process.</span></span> <span data-ttu-id="aff9e-118">Событие триггера записи может быть временным файлом записи, который направляется на конкретный уровень или шаблон данных, происходящий в захваченном кадре.</span><span class="sxs-lookup"><span data-stu-id="aff9e-118">The capture trigger event can be a temporary capture file that is directed to a specific level or data pattern that occurs in a captured frame.</span></span>

</dd> <dt>

<span data-ttu-id="aff9e-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**захваченные данные**</span><span class="sxs-lookup"><span data-stu-id="aff9e-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**captured data**</span></span>
</dt> <dd>

<span data-ttu-id="aff9e-120">Кадры с определенным набором критериев.</span><span class="sxs-lookup"><span data-stu-id="aff9e-120">Frames that have a defined set of criteria.</span></span> <span data-ttu-id="aff9e-121">Кадры данных содержатся во временном файле записи.</span><span class="sxs-lookup"><span data-stu-id="aff9e-121">The data frames are contained in a temporary capture file.</span></span>

</dd> <dt>

<span data-ttu-id="aff9e-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**Статистика диалога**</span><span class="sxs-lookup"><span data-stu-id="aff9e-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**conversation statistics**</span></span>
</dt> <dd>

<span data-ttu-id="aff9e-123">Статистика сетевого трафика, сохраненная во время записи.</span><span class="sxs-lookup"><span data-stu-id="aff9e-123">Statistics of network traffic saved during a capture.</span></span> <span data-ttu-id="aff9e-124">Эти статистические данные включают сведения о станциях и сеансах, которые начинаются с момента запуска процесса записи и заканчиваются после остановки записи.</span><span class="sxs-lookup"><span data-stu-id="aff9e-124">These statistics include station and session information beginning when the capture process starts, and ending when the capture stops.</span></span> <span data-ttu-id="aff9e-125">Если вы приостанавливаете процесс записи, сетевой монитор продолжает добавлять статистику при возобновлении процесса.</span><span class="sxs-lookup"><span data-stu-id="aff9e-125">If you pause the capture process, Network Monitor continues to add statistics when you resume the process.</span></span> <span data-ttu-id="aff9e-126">Чтобы получить статистику диалога, вызовите метод **жетконверсатионстатистикс** для интерфейса, который вы используете.</span><span class="sxs-lookup"><span data-stu-id="aff9e-126">To retrieve conversation statistics, call the **GetConversationStatistics** method for the interface you are using.</span></span>

</dd> </dl>

 

 



