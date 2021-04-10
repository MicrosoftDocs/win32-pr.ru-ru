---
description: API печати GDI предоставляет приложения с интерфейсом печати, не зависящим от устройства.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API печати GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264453"
---
# <a name="gdi-print-api"></a><span data-ttu-id="0b186-103">API печати GDI</span><span class="sxs-lookup"><span data-stu-id="0b186-103">GDI Print API</span></span>

<span data-ttu-id="0b186-104">API печати GDI предоставляет приложения с интерфейсом печати, не зависящим от устройства.</span><span class="sxs-lookup"><span data-stu-id="0b186-104">The GDI Print API provides applications with a device-independent printing interface.</span></span> <span data-ttu-id="0b186-105">Используйте этот интерфейс, если приложение использует GDI для отрисовки текста и графики.</span><span class="sxs-lookup"><span data-stu-id="0b186-105">Use this interface if the application uses GDI to render text and graphics.</span></span>

<span data-ttu-id="0b186-106">Если вы пишете приложения для Windows Vista или более поздних версий Windows, рассмотрите возможность использования [API документов XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) и [API печати XPS](xps-printing.md) для использования высокопроизводительных графических интерфейсов, поддерживаемых драйверами печати XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="0b186-106">If you write applications for Windows Vista or later versions of Windows, consider using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and the [XPS Print API](xps-printing.md) to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span>

<span data-ttu-id="0b186-107">В этом разделе содержатся сведения о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="0b186-107">This section provides information about the following topics.</span></span>



| <span data-ttu-id="0b186-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="0b186-108">Topic</span></span>                                                                                             | <span data-ttu-id="0b186-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0b186-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b186-110">Сведения об API печати GDI</span><span class="sxs-lookup"><span data-stu-id="0b186-110">About the GDI Print API</span></span>](about-the-gdi-print-api.md)<br/>                                 | <span data-ttu-id="0b186-111">Общие сведения о функции печати GDI.</span><span class="sxs-lookup"><span data-stu-id="0b186-111">An overview of the GDI printing functionality.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="0b186-112">Использование API печати GDI</span><span class="sxs-lookup"><span data-stu-id="0b186-112">Using the GDI Print API</span></span>](using-the-printing-functions.md)<br/>                            | <span data-ttu-id="0b186-113">Сведения об использовании API печати GDI в приложении.</span><span class="sxs-lookup"><span data-stu-id="0b186-113">Information about using the GDI Print API in an application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="0b186-114">Справочник по API печати GDI</span><span class="sxs-lookup"><span data-stu-id="0b186-114">GDI Print API Reference</span></span>](gdi-print-api-reference.md)<br/>                                 | <span data-ttu-id="0b186-115">Подробное описание функций, структур и других элементов API-интерфейса печати GDI.</span><span class="sxs-lookup"><span data-stu-id="0b186-115">Detailed descriptions of the functions, structures, and other elements of the GDI Print API.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="0b186-116">Конвертер документов XPS (Майкрософт) (МКСДК)</span><span class="sxs-lookup"><span data-stu-id="0b186-116">Microsoft XPS Document Converter (MXDC)</span></span>](microsoft-xps-document-converter--mxdc-.md)<br/> | <span data-ttu-id="0b186-117">[Конвертер документов XPS (Майкрософт) (мксдк)](microsoft-xps-document-converter--mxdc-.md) — это компонент, позволяющий ПРИЛОЖЕНИЯМ использовать API печати GDI с принтерами с драйвером печати XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="0b186-117">The [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) is a component that enables applications to use the GDI Print API with printers that have an XPSDrv Print Driver.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="0b186-118">Модуль записи XPS-документов (Майкрософт) (МКСДВ)</span><span class="sxs-lookup"><span data-stu-id="0b186-118">Microsoft XPS Document Writer (MXDW)</span></span>](microsoft-xps-document-writer.md)<br/>              | <span data-ttu-id="0b186-119">[Модуль записи XPS-документов (Майкрософт) (мксдв)](microsoft-xps-document-writer.md) предоставляет приложения с функциями "Сохранить как XPS" или "экспортировать в XPS".</span><span class="sxs-lookup"><span data-stu-id="0b186-119">The [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) provides applications with "save as XPS" or "export to XPS" functionality.</span></span> <span data-ttu-id="0b186-120">Приложения, которые изначально не создают содержимое документа XPS, могут использовать МКСДВ для создания файлов документов XPS без использования [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b186-120">Applications that do not natively create XPS document content can use the MXDW to create XPS document files without using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="0b186-121">Однако API документа XPS предоставляет приложению возможность использовать высокопроизводительные графические интерфейсы, поддерживаемые драйверами печати XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="0b186-121">The XPS Document API, however, provides an application with the ability to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span><br/> |



 

<span data-ttu-id="0b186-122">На следующей схеме показана связь интерфейса API печати GDI с другими интерфейсами API печати, которые может использовать приложение.</span><span class="sxs-lookup"><span data-stu-id="0b186-122">The following diagram shows the relationship of the GDI Print API to the other print APIs that an application can use.</span></span>

![Схема, показывающая связь API печати GDI с другими API-интерфейсами печати, которые может использовать приложение Win32](images/print-apis-gdi.png)

## <a name="related-topics"></a><span data-ttu-id="0b186-124">См. также</span><span class="sxs-lookup"><span data-stu-id="0b186-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b186-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="0b186-125">**AddJob**</span></span>](addjob.md)
</dt> <dt>

<span data-ttu-id="0b186-126">[API документов XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b186-126">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b186-127">API печати XPS</span><span class="sxs-lookup"><span data-stu-id="0b186-127">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="0b186-128">API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="0b186-128">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="0b186-129">API билетов на печать</span><span class="sxs-lookup"><span data-stu-id="0b186-129">Print Ticket API</span></span>](print-ticket-api.md)
</dt> </dl>

 

