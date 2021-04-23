---
description: В этом разделе содержится список кодов возврата WMI, символьных констант, литеральных значений и описаний. Эти коды могут возвращаться сценариями, приложениями C++ или командами WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Коды возврата WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692685"
---
# <a name="wmi-return-codes"></a><span data-ttu-id="79a12-104">Коды возврата WMI</span><span class="sxs-lookup"><span data-stu-id="79a12-104">WMI Return Codes</span></span>

<span data-ttu-id="79a12-105">В этом разделе содержится список кодов возврата WMI, символьных констант, литеральных значений и описаний.</span><span class="sxs-lookup"><span data-stu-id="79a12-105">This section provides a list of the WMI return codes, symbolic constants, literal values, and descriptions.</span></span> <span data-ttu-id="79a12-106">Эти коды могут возвращаться сценариями, приложениями C++ или командами [**WMIC**](wmic.md) .</span><span class="sxs-lookup"><span data-stu-id="79a12-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md) commands.</span></span>

<span data-ttu-id="79a12-107">При возникновении ошибки Инструментарий WMI возвращает один из следующих кодов ошибок в виде 32-разрядного значения, где две старшие биты указывают код серьезности сообщения.</span><span class="sxs-lookup"><span data-stu-id="79a12-107">If an error occurs, WMI returns one of the following error codes as a 32-bit value where the two high-order bits indicate the severity code of the message.</span></span>

<dl> <dt>

<span data-ttu-id="79a12-108"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="79a12-108"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="79a12-109">Успешно</span><span class="sxs-lookup"><span data-stu-id="79a12-109">Success</span></span>

</dd> <dt>

<span data-ttu-id="79a12-110"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="79a12-110"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="79a12-111">Informational</span><span class="sxs-lookup"><span data-stu-id="79a12-111">Informational</span></span>

</dd> <dt>

<span data-ttu-id="79a12-112"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="79a12-112"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="79a12-113">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="79a12-113">Warning</span></span>

</dd> <dt>

<span data-ttu-id="79a12-114"><span id="3"></span>3-5</span><span class="sxs-lookup"><span data-stu-id="79a12-114"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="79a12-115">Ошибка</span><span class="sxs-lookup"><span data-stu-id="79a12-115">Error</span></span>

</dd> </dl>

> [!Note]
>
> <span data-ttu-id="79a12-116">Если инструментарий WMI возвращает сообщения об ошибках, имейте в виду, что они могут не указывать на проблемы в службе WMI или в поставщиках WMI.</span><span class="sxs-lookup"><span data-stu-id="79a12-116">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="79a12-117">Сбои могут исходить из других частей операционной системы и возникать как ошибки через инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="79a12-117">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="79a12-118">При любых обстоятельствах не удаляйте репозиторий WMI как первое действие, поскольку удаление репозитория может привести к повреждению системы или установке приложений.</span><span class="sxs-lookup"><span data-stu-id="79a12-118">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="79a12-119">Чтобы получить дополнительные сведения об источнике проблемы, скачайте и запустите программу командной строки для диагностики [служебная программа для диагностики WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="79a12-119">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="79a12-120">Это средство создает отчет, который обычно может изолировать источник проблемы и предоставить инструкции по ее устранению.</span><span class="sxs-lookup"><span data-stu-id="79a12-120">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="79a12-121">Этот отчет также помогает в работе со службой поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="79a12-121">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="79a12-122">Служебная программа для диагностики WMI можно скачать [здесь](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="79a12-122">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

-   [<span data-ttu-id="79a12-123">**Константы ошибок WMI**</span><span class="sxs-lookup"><span data-stu-id="79a12-123">**WMI Error Constants**</span></span>](wmi-error-constants.md)
-   [<span data-ttu-id="79a12-124">**Константы WMI, отличные от ошибок**</span><span class="sxs-lookup"><span data-stu-id="79a12-124">**WMI Non-Error Constants**</span></span>](wmi-non-error-constants.md)

 

 



