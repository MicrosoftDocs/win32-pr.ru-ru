---
description: Предоставляет интерфейс диспетчера очереди печати. Приложения могут использовать этот API для отправки XPS-документов на принтер.
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: API печати XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711684"
---
# <a name="xps-print-api"></a><span data-ttu-id="d0066-104">API печати XPS</span><span class="sxs-lookup"><span data-stu-id="d0066-104">XPS Print API</span></span>

<span data-ttu-id="d0066-105">\[API печати XPS не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="d0066-105">\[The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d0066-106">Вместо этого клиентские приложения должны использовать [API пакета печати документов](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="d0066-106">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="d0066-107">Предоставляет интерфейс диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="d0066-107">Provides an interface to the print spooler.</span></span> <span data-ttu-id="d0066-108">Приложения могут использовать этот API для отправки XPS-документов на принтер.</span><span class="sxs-lookup"><span data-stu-id="d0066-108">Applications can use this API to send XPS documents to a printer.</span></span>

<span data-ttu-id="d0066-109">В этом разделе содержатся сведения о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="d0066-109">This section contains information about the following topics.</span></span>

<dl>

[<span data-ttu-id="d0066-110">Сведения об API печати XPS</span><span class="sxs-lookup"><span data-stu-id="d0066-110">About the XPS Print API</span></span>](about-xps-print-api.md)  
[<span data-ttu-id="d0066-111">Использование API печати XPS</span><span class="sxs-lookup"><span data-stu-id="d0066-111">Using the XPS Print API</span></span>](using-the-xps-print-api.md)  
[<span data-ttu-id="d0066-112">Справочник по API печати XPS</span><span class="sxs-lookup"><span data-stu-id="d0066-112">XPS Print API Reference</span></span>](xpsprint-interfaces.md)  
</dl>

<span data-ttu-id="d0066-113">Собственные приложения Windows, которые создают документы XPS, например, с помощью [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)), могут использовать API печати XPS для отправки содержимого XPS-документа на принтер.</span><span class="sxs-lookup"><span data-stu-id="d0066-113">Native Windows applications that create XPS documents, such as by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)), can use the XPS Print API to send XPS document content to a printer.</span></span>

<span data-ttu-id="d0066-114">На следующей схеме показана связь API печати XPS с другими интерфейсами API печати, которые может использовать собственное приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="d0066-114">The following diagram shows the relationship of the XPS Print API to the other Print APIs that a native Windows application can use.</span></span>

![Схема, показывающая связь API печати XPS с другими интерфейсами API печати, которые может использовать собственное приложение Windows](images/print-apis-xps.png)

## <a name="related-topics"></a><span data-ttu-id="d0066-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d0066-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0066-117">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="d0066-117">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="d0066-118">API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="d0066-118">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="d0066-119">API билетов на печать</span><span class="sxs-lookup"><span data-stu-id="d0066-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="d0066-120">API печати GDI</span><span class="sxs-lookup"><span data-stu-id="d0066-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 
