---
title: Возвращаемые значения СИСМОН
description: Ниже приведен список возвращаемых значений системного монитора, определенных в Смонмсг. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413377"
---
# <a name="sysmon-return-values"></a><span data-ttu-id="d92d6-103">Возвращаемые значения СИСМОН</span><span class="sxs-lookup"><span data-stu-id="d92d6-103">SYSMON Return Values</span></span>

<span data-ttu-id="d92d6-104">Ниже приведен список возвращаемых значений системного монитора, определенных в Смонмсг. h.</span><span class="sxs-lookup"><span data-stu-id="d92d6-104">The following is a list of the System Monitor return values that are defined in Smonmsg.h.</span></span>



| <span data-ttu-id="d92d6-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d92d6-105">Return value</span></span>                                       | <span data-ttu-id="d92d6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d92d6-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d92d6-107">\_ \_ \_ Путь к счетчику состояния смон дупл \_ (0xC0001388)</span><span class="sxs-lookup"><span data-stu-id="d92d6-107">SMON\_STATUS\_DUPL\_COUNTER\_PATH (0xC0001388)</span></span>     | <span data-ttu-id="d92d6-108">Коллекция счетчиков уже содержит указанный счетчик.</span><span class="sxs-lookup"><span data-stu-id="d92d6-108">The counter collection already contains the specified counter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="d92d6-109">\_Состояние смон \_ нет \_ \_ объекта сисмон (0xC0001389)</span><span class="sxs-lookup"><span data-stu-id="d92d6-109">SMON\_STATUS\_NO\_SYSMON\_OBJECT (0xC0001389)</span></span>      | <span data-ttu-id="d92d6-110">Параметры не содержат никаких полных объектов HTML системного монитора.</span><span class="sxs-lookup"><span data-stu-id="d92d6-110">The settings do not contain any complete System Monitor HTML objects.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="d92d6-111">\_Состояние смон \_ слишком \_ мало \_ выборок (0xC000138A)</span><span class="sxs-lookup"><span data-stu-id="d92d6-111">SMON\_STATUS\_TOO\_FEW\_SAMPLES (0xC000138A)</span></span>       | <span data-ttu-id="d92d6-112">Указанный файл журнала содержит менее двух выборок данных.</span><span class="sxs-lookup"><span data-stu-id="d92d6-112">The specified log file contains fewer than two data samples.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="d92d6-113">\_ \_ \_ Предельный размер файла журнала состояния смон \_ \_ (0xC000138B)</span><span class="sxs-lookup"><span data-stu-id="d92d6-113">SMON\_STATUS\_LOG\_FILE\_SIZE\_LIMIT (0xC000138B)</span></span>  | <span data-ttu-id="d92d6-114">Указанный файл журнала превышает ограничения на размер элемента управления системного монитора.</span><span class="sxs-lookup"><span data-stu-id="d92d6-114">The specified log file exceeds the size limits of the System Monitor control.</span></span> <span data-ttu-id="d92d6-115">Если в данный момент выбран файл журнала, выберите текущее действие в качестве источника данных, чтобы выгрузить текущий файл журнала, а затем повторно выбрать указанный файл журнала.</span><span class="sxs-lookup"><span data-stu-id="d92d6-115">If a log file is currently selected, select current activity as the data source in order to unload the current log file, then reselect the specified log file.</span></span> |
| <span data-ttu-id="d92d6-116">\_ \_ \_ Источник данных файла журнала состояния смон \_ \_ (0xC000138C)</span><span class="sxs-lookup"><span data-stu-id="d92d6-116">SMON\_STATUS\_LOG\_FILE\_DATA\_SOURCE (0xC000138C)</span></span> | <span data-ttu-id="d92d6-117">Чтобы добавить новый файл журнала в источник данных, необходимо изменить тип источника данных на тип, отличный от Сисмонлогфилес.</span><span class="sxs-lookup"><span data-stu-id="d92d6-117">To add a new log file to the data source, the data source type must be changed to a type other than sysmonLogFiles.</span></span>                                                                                                                          |
| <span data-ttu-id="d92d6-118">СМОН \_ состояния \_ дупл \_ \_ \_ путь к файлу журнала (0xC000138D)</span><span class="sxs-lookup"><span data-stu-id="d92d6-118">SMON\_STATUS\_DUPL\_LOG\_FILE\_PATH (0xC000138D)</span></span>   | <span data-ttu-id="d92d6-119">Коллекция файлов журнала уже содержит указанный файл журнала.</span><span class="sxs-lookup"><span data-stu-id="d92d6-119">The log file collection already contains the specified log file.</span></span>                                                                                                                                                                             |



 

<span data-ttu-id="d92d6-120">Описание дополнительных возвращаемых значений, возвращаемых системным монитором, см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes) и [вспомогательные коды ошибок данных производительности](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span><span class="sxs-lookup"><span data-stu-id="d92d6-120">For a description of additional return values returned by System Monitor, see [System Error Codes](/windows/desktop/Debug/system-error-codes) and [Performance Data Helper Error Codes](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span></span>

 

 