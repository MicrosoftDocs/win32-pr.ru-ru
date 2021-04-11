---
description: '&XPS \# 160; Печать&\# 160; API предоставляет интерфейс диспетчера очереди печати, который приложения могут использовать для печати заданий, отправляющих XPS-документы на принтер.'
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Сведения об API печати XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156450"
---
# <a name="about-the-xps-print-api"></a><span data-ttu-id="07ce5-103">Сведения об API печати XPS</span><span class="sxs-lookup"><span data-stu-id="07ce5-103">About the XPS Print API</span></span>

<span data-ttu-id="07ce5-104">[API печати XPS](xps-printing.md) предоставляет интерфейс диспетчера очереди печати, который приложения могут использовать для печати заданий, отправляющих XPS-документы на принтер.</span><span class="sxs-lookup"><span data-stu-id="07ce5-104">The [XPS Print API](xps-printing.md) provides an interface to the print spooler that applications can use to print jobs that send XPS documents to a printer.</span></span>

<span data-ttu-id="07ce5-105">Если принтер назначения использует драйвер принтера XPSDrv, API печати XPS дает возможность драйверу принтера XPSDrv принимать события документов, так как диспетчер очереди печати обрабатывает задание печати.</span><span class="sxs-lookup"><span data-stu-id="07ce5-105">If the destination printer uses an XPSDrv printer driver, the XPS Print API makes it possible for the XPSDrv printer driver to receive document events as the print spooler processes a print job.</span></span> <span data-ttu-id="07ce5-106">Описание событий документа, отправляемых в драйвер принтера XPSDrv, см. в разделе [события документа драйвера XPS](/windows-hardware/drivers/print/xps-driver-document-events).</span><span class="sxs-lookup"><span data-stu-id="07ce5-106">For a description of the document events that are sent to the XPSDrv printer driver see [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).</span></span>

<span data-ttu-id="07ce5-107">Если принтер назначения использует драйвер принтера GDI, [API печати XPS](xps-printing.md) позволяет системе обменять необходимое преобразование данных задания печати из формата XPS в формат расширенного метафайла (EMF), используемый драйвером принтера GDI.</span><span class="sxs-lookup"><span data-stu-id="07ce5-107">If the destination printer uses a GDI printer driver, the [XPS Print API](xps-printing.md) lets the system handle the necessary conversion of the print job data from XPS format to the Enhanced Metafile (EMF) format that the GDI printer driver uses.</span></span> <span data-ttu-id="07ce5-108">Описание событий документа драйвера принтера GDI см. в разделе [функция документевент](documentevent.md).</span><span class="sxs-lookup"><span data-stu-id="07ce5-108">For a description of the GDI printer driver document events see [DocumentEvent Function](documentevent.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="07ce5-109">См. также</span><span class="sxs-lookup"><span data-stu-id="07ce5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07ce5-110">Использование API печати XPS</span><span class="sxs-lookup"><span data-stu-id="07ce5-110">Using the XPS Print API</span></span>](using-the-xps-print-api.md)
</dt> <dt>

[<span data-ttu-id="07ce5-111">Справочник по API печати XPS</span><span class="sxs-lookup"><span data-stu-id="07ce5-111">XPS Print API Reference</span></span>](xpsprint-api.md)
</dt> </dl>

 

 
