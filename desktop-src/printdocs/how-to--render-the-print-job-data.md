---
description: В этом разделе описывается Визуализация данных программы для печати.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: Как отобразить данные задания печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913151"
---
# <a name="how-to-render-print-job-data"></a><span data-ttu-id="9701f-103">Как отобразить данные задания печати</span><span class="sxs-lookup"><span data-stu-id="9701f-103">How To: Render Print Job Data</span></span>

<span data-ttu-id="9701f-104">В этом разделе описывается Визуализация данных программы для печати.</span><span class="sxs-lookup"><span data-stu-id="9701f-104">This topic describes how to render the program data to be printed.</span></span> <span data-ttu-id="9701f-105">В этом разделе подробно объясняется, как визуализировать определенные графические или текстовые изображения.</span><span class="sxs-lookup"><span data-stu-id="9701f-105">This topic does not explain in detail about how to render specific graphics or text images.</span></span> <span data-ttu-id="9701f-106">Вместо этого он описывает, как управлять данными программы и визуализировать их как документ XPS, который отправляется на принтер с помощью [API печати XPS](xps-printing.md).</span><span class="sxs-lookup"><span data-stu-id="9701f-106">Instead, it describes how to manage the program data and render it as an XPS document, which it sends to a printer by using the [XPS Print API](xps-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="9701f-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="9701f-107">Overview</span></span>

<span data-ttu-id="9701f-108">Отрисовка данных заданий печати для печати предполагает получение данных программы, таких как текст, изображения и форматирование, и их преобразование в формат, совместимый с принтером назначения.</span><span class="sxs-lookup"><span data-stu-id="9701f-108">Rendering print job data for printing involves taking the program-specific data, such as text, images, and formatting, and converting them into a format that is compatible with the destination printer.</span></span> <span data-ttu-id="9701f-109">Программа, отправляющая данные на принтер, должна отправлять их в формате, который требуется драйверу принтера.</span><span class="sxs-lookup"><span data-stu-id="9701f-109">The program that sends the data to the printer must send it in the format that the printer driver requires.</span></span>

<span data-ttu-id="9701f-110">Используйте [API печати XPS](xps-printing.md) для отправки данных на принтер, и для этого требуется, чтобы данные были отформатированы как документ XPS.</span><span class="sxs-lookup"><span data-stu-id="9701f-110">Use the [XPS Print API](xps-printing.md) to send the data to the printer and it requires the data to be formatted as an XPS document.</span></span> <span data-ttu-id="9701f-111">Для создания содержимого XPS-документа, необходимого API печати XPS, образец программы использует [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9701f-111">To produce the XPS document content that the XPS Print API needs, the sample program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span>

<span data-ttu-id="9701f-112">Если содержимое программы имеет формат, несовместимый с принтером, он должен быть визуализирован перед отправкой на принтер.</span><span class="sxs-lookup"><span data-stu-id="9701f-112">If the program content is in a format that is not compatible with a printer, it will need to be rendered before it is sent to the printer.</span></span> <span data-ttu-id="9701f-113">Если программа использует [API документов XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) для управления содержимым программы, содержимое программы будет иметь формат, который можно отправить непосредственно в [API печати XPS](xps-printing.md) и не будет требовать дополнительной подготовки к просмотру перед отправкой на принтер.</span><span class="sxs-lookup"><span data-stu-id="9701f-113">If the program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to manage its program content, the program content will be in a format that can be sent directly to the [XPS Print API](xps-printing.md) and will not require any additional rendering before you send it to the printer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9701f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9701f-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9701f-115">[API документов XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9701f-115">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9701f-116">API печати XPS</span><span class="sxs-lookup"><span data-stu-id="9701f-116">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

 
