---
description: API диспетчера очереди печати предоставляет интерфейс диспетчера очереди печати для приложений, управляющих принтерами и заданиями печати.
ms.assetid: b6cc0c9d-9f28-4e80-b847-39c72d98bed6
title: API диспетчера очереди печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7287b9da3ac19d2ab9c39152d5917960e465e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081160"
---
# <a name="print-spooler-api"></a><span data-ttu-id="6e9c1-103">API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="6e9c1-103">Print Spooler API</span></span>

<span data-ttu-id="6e9c1-104">API диспетчера очереди печати предоставляет интерфейс диспетчера очереди печати для приложений, управляющих принтерами и заданиями печати.</span><span class="sxs-lookup"><span data-stu-id="6e9c1-104">The Print Spooler API provides an interface to the print spooler for applications to manage printers and print jobs.</span></span>

<span data-ttu-id="6e9c1-105">API диспетчера очереди печати используется приложением в рамках его программирования, а не непосредственно конечными пользователями.</span><span class="sxs-lookup"><span data-stu-id="6e9c1-105">The Print Spooler API is used by an application as part of its programming and not directly by end users.</span></span>

<span data-ttu-id="6e9c1-106">В этом разделе содержатся сведения о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="6e9c1-106">This section contains information about the following topics.</span></span>



| <span data-ttu-id="6e9c1-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="6e9c1-107">Topic</span></span>                                                                                             | <span data-ttu-id="6e9c1-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6e9c1-108">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e9c1-109">Справочник по API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="6e9c1-109">Print Spooler API Reference</span></span>](printing-and-print-spooler-reference.md)<br/>                | <span data-ttu-id="6e9c1-110">Подробные сведения о функциях, структурах и других элементах API диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="6e9c1-110">Detailed information about the functions, structures, and other elements of the Print Spooler API.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="6e9c1-111">Ссылка на асинхронную печать уведомлений</span><span class="sxs-lookup"><span data-stu-id="6e9c1-111">Asynchronous Printing Notification Reference</span></span>](asynchronous-printing-notification.md)<br/> | <span data-ttu-id="6e9c1-112">Описание функций, интерфейсов и перечислений, используемых для асинхронного взаимодействия между приложениями и компонентами, размещенными в диспетчере очереди печати, такими как драйверы принтеров и мониторы портов.</span><span class="sxs-lookup"><span data-stu-id="6e9c1-112">Descriptions of the functions, interfaces, and enumerations that are used in asynchronous communication between applications and print-spooler-hosted components, such as printer drivers and port monitors.</span></span><br/> |
| [<span data-ttu-id="6e9c1-113">Справочник по установке драйвера принтера</span><span class="sxs-lookup"><span data-stu-id="6e9c1-113">Printer Driver Installation Reference</span></span>](printer-driver-installation-reference.md)<br/>     | <span data-ttu-id="6e9c1-114">Описание функций, устанавливающих и настроив драйверы принтеров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6e9c1-114">Describes the functions that install and configure printer drivers on a computer.</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="6e9c1-115">На следующей схеме показана связь API диспетчера очереди печати с другими интерфейсами API печати, которые может использовать собственное приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="6e9c1-115">The following diagram shows the relationship of the Print Spooler API to the other Print APIs that a native Windows application can use.</span></span>

![Схема, показывающая связь API диспетчера очереди печати с другими интерфейсами API печати, которые может использовать собственное приложение Windows](images/print-apis-ps.png)

## <a name="related-topics"></a><span data-ttu-id="6e9c1-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6e9c1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e9c1-118">API печати XPS</span><span class="sxs-lookup"><span data-stu-id="6e9c1-118">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="6e9c1-119">API билетов на печать</span><span class="sxs-lookup"><span data-stu-id="6e9c1-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="6e9c1-120">API печати GDI</span><span class="sxs-lookup"><span data-stu-id="6e9c1-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 




