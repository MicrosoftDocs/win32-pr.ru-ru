---
description: .
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Интерфейсы API печати XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828e999417354678d77ad1de8c29beb5956f7762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812562"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="f8e76-103">Интерфейсы API печати XPS</span><span class="sxs-lookup"><span data-stu-id="f8e76-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="f8e76-104">\[Интерфейсы, описанные в этом разделе, являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="f8e76-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="f8e76-105">Вместо этого клиентские приложения должны использовать [API пакета печати документов](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="f8e76-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="f8e76-106">\[Икспспринтжоб не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="f8e76-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f8e76-107">\]</span><span class="sxs-lookup"><span data-stu-id="f8e76-107">\]</span></span>

<span data-ttu-id="f8e76-108">\[Икспспринтжобстреам не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="f8e76-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f8e76-109">\]</span><span class="sxs-lookup"><span data-stu-id="f8e76-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f8e76-110">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="f8e76-110">In this section</span></span>



| <span data-ttu-id="f8e76-111">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f8e76-111">Interface</span></span>                                                   | <span data-ttu-id="f8e76-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f8e76-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8e76-113">**икспспринтжоб**</span><span class="sxs-lookup"><span data-stu-id="f8e76-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="f8e76-114">Предоставляет доступ к выполняемому в данный момент заданию печати.</span><span class="sxs-lookup"><span data-stu-id="f8e76-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="f8e76-115">**икспспринтжобстреам**</span><span class="sxs-lookup"><span data-stu-id="f8e76-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="f8e76-116">Потоковый интерфейс только для записи, в который приложение записывает данные задания печати.</span><span class="sxs-lookup"><span data-stu-id="f8e76-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f8e76-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f8e76-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8e76-118">Документы</span><span class="sxs-lookup"><span data-stu-id="f8e76-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="f8e76-119">XPS</span><span class="sxs-lookup"><span data-stu-id="f8e76-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

