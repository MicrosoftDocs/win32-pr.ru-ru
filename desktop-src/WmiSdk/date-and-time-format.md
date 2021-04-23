---
description: Описывает формат даты и времени модель CIM (CIM), используемый WMI. Этот формат не зависит от языкового стандарта, поэтому скрипты, использующие дату и время, могут выполняться во многих часовых поясах.
ms.assetid: be239bf8-88a3-47bc-ae4f-49a5195e7a7d
ms.tgt_platform: multiple
title: Формат даты и времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e8f97930efa33942fe87b2109aa7cd7ba9d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156006"
---
# <a name="date-and-time-format"></a><span data-ttu-id="da7a9-104">Формат даты и времени</span><span class="sxs-lookup"><span data-stu-id="da7a9-104">Date and Time Format</span></span>

<span data-ttu-id="da7a9-105">Инструментарий WMI использует форматы даты и времени, определенные спецификацией распределенного управления Task Force ([DMTF.org](https://www.dmtf.org/)) модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="da7a9-105">WMI uses the date and time formats defined by the Distributed Management Task Force ([DMTF.org](https://www.dmtf.org/)) Common Information Model (CIM) specification.</span></span>

<span data-ttu-id="da7a9-106">Формат **\_ даты и времени CIM** реализуется в Microsoft [MOF-файл (MOF)](managed-object-format--mof-.md) типом данных [DateTime](datetime.md) MOF.</span><span class="sxs-lookup"><span data-stu-id="da7a9-106">The **CIM\_DATETIME** format is implemented in the Microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) by the [DATETIME](datetime.md) MOF datatype.</span></span> <span data-ttu-id="da7a9-107">Форматы даты и времени могут также выражать интервал времени.</span><span class="sxs-lookup"><span data-stu-id="da7a9-107">The date and time formats can also express an interval of time.</span></span>

<span data-ttu-id="da7a9-108">Дополнительные сведения о форматах WMI см. в разделе [Формат](interval-format.md) [ \_ даты](cim-datetime.md) и времени CIM.</span><span class="sxs-lookup"><span data-stu-id="da7a9-108">For more information about WMI formats, see [CIM\_DATETIME](cim-datetime.md) and [Interval Format](interval-format.md).</span></span>

<span data-ttu-id="da7a9-109">Дополнительные сведения о преобразовании в формат DATETIME WMI и из него см. в разделе [**SWbemDateTime**](swbemdatetime.md) и статья на сайте TechNet Скриптцентер [о времени (и о датах)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="da7a9-109">For more information about converting to and from the WMI DATETIME format, see [**SWbemDateTime**](swbemdatetime.md) and the article on TechNet ScriptCenter [It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="da7a9-110">См. также</span><span class="sxs-lookup"><span data-stu-id="da7a9-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da7a9-111">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="da7a9-111">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



