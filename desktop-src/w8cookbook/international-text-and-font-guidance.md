---
title: Международные правила для текста и шрифтов
description: Международные правила для текста и шрифтов
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412980"
---
# <a name="international-text-and-font-guidance"></a><span data-ttu-id="a0a18-103">Международные правила для текста и шрифтов</span><span class="sxs-lookup"><span data-stu-id="a0a18-103">International text and font guidance</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a0a18-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="a0a18-104">Affected Platforms</span></span>

<dl> <span data-ttu-id="a0a18-105">Клиенты — Windows 8.1 Windows 8 \|</span><span class="sxs-lookup"><span data-stu-id="a0a18-105">Clients - Windows 8 \| Windows 8.1</span></span>  
<span data-ttu-id="a0a18-106">Серверы — Windows Server 2012 \| Windows server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a0a18-106">Servers - Windows Server 2012 \| Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="a0a18-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a0a18-107">Description</span></span>

<span data-ttu-id="a0a18-108">С момента выпуска Windows 2000 в каждом основном выпуске Windows была добавлена поддержка просмотра текста для новых сценариев.</span><span class="sxs-lookup"><span data-stu-id="a0a18-108">Since before Windows 2000, text-display support for new scripts has been added in each major release of Windows.</span></span> <span data-ttu-id="a0a18-109">Описания изменений, внесенных в каждом основном выпуске, можно найти в статье [Поддержка скриптов и шрифтов для Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) в [центре разработки Go Global](https://msdn.microsoft.com/goglobal/default).</span><span class="sxs-lookup"><span data-stu-id="a0a18-109">You can find descriptions of the changes made in each major release in the [Script and Font Support for Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) article at the [Go Global Development Center](https://msdn.microsoft.com/goglobal/default).</span></span>

<span data-ttu-id="a0a18-110">Обратите внимание, что поддержка сценария может потребовать внесения определенных изменений в компоненты стека текста, а также изменения шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a0a18-110">Note that support for a script may require certain changes to text stack components as well as changes to fonts.</span></span> <span data-ttu-id="a0a18-111">В операционной системе Windows имеется множество компонентов стека текста: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 и др.</span><span class="sxs-lookup"><span data-stu-id="a0a18-111">The Windows operating system has many text stack components: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32, and others.</span></span> <span data-ttu-id="a0a18-112">Предоставленные сведения в основном относятся к GDI и DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="a0a18-112">The information provided pertains primarily to GDI and DirectWrite.</span></span> <span data-ttu-id="a0a18-113">Он также применяется к платформам пользовательского интерфейса, таким как RichEdit или агенту подготовки отчетов MSHTML, используемому для приложений Магазина Windows 8 и для отрисовки веб-содержимого, хотя эти компоненты могут демонстрировать определенные различия.</span><span class="sxs-lookup"><span data-stu-id="a0a18-113">It is also generally applicable to UI frameworks such as RichEdit or the MSHTML rendering agent used for Windows 8 Store apps and for rendering web content, though those components may exhibit certain differences.</span></span>

## <a name="best-practices"></a><span data-ttu-id="a0a18-114">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="a0a18-114">Best Practices</span></span>

<span data-ttu-id="a0a18-115">**Типографские рекомендации для разработчиков**</span><span class="sxs-lookup"><span data-stu-id="a0a18-115">**Typography guidance for developers**</span></span>

<span data-ttu-id="a0a18-116">Типография — это основа языка разработки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a0a18-116">Typography is at the heart of the Microsoft design language.</span></span> <span data-ttu-id="a0a18-117">Каждый из принципов проектирования Майкрософт усиливает важность оформления.</span><span class="sxs-lookup"><span data-stu-id="a0a18-117">Each of the Microsoft design principles reinforces the importance of typography.</span></span> <span data-ttu-id="a0a18-118">В первый раз разработчики приложений имеют набор платформ, поддерживающих расширенные типографские функции.</span><span class="sxs-lookup"><span data-stu-id="a0a18-118">For the first time, app developers have a set of frameworks that support advanced typographic features.</span></span> <span data-ttu-id="a0a18-119">Перейдите к разделу [Отображение и редактирование текста](/previous-versions/windows/apps/hh465442(v=win.10)) , чтобы узнать, как использовать JavaScript и HTML для отображения и редактирования текста в приложениях для Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="a0a18-119">Go to [Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10)) for information about how to use JavaScript and HTML to display and edit text in Windows Store apps.</span></span>

<span data-ttu-id="a0a18-120">**Метрики шрифта**</span><span class="sxs-lookup"><span data-stu-id="a0a18-120">**Font metrics**</span></span>

<span data-ttu-id="a0a18-121">Метрики шрифтов — это область определенного важности для разработчиков приложений.</span><span class="sxs-lookup"><span data-stu-id="a0a18-121">Font metrics are an area of particular importance to application developers.</span></span> <span data-ttu-id="a0a18-122">Файлы шрифтов содержат различные значения, связанные с вертикальными и горизонтальными метриками.</span><span class="sxs-lookup"><span data-stu-id="a0a18-122">Font files contain various values related to vertical and horizontal metrics.</span></span> <span data-ttu-id="a0a18-123">Эти значения задокументированы в [спецификации OpenType](https://www.microsoft.com/typography/otspec/) , и они предоставляются с помощью различных интерфейсов API, которые находятся в [ \_ \_ структуре метрик шрифта дврите](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) и в [структуре текстметрик](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span><span class="sxs-lookup"><span data-stu-id="a0a18-123">These values are documented in the [OpenType specification](https://www.microsoft.com/typography/otspec/) and these are exposed via a variety of APIs found at [DWRITE\_FONT\_METRICS structure](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) and at [TEXTMETRIC Structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span></span>

## <a name="resources"></a><span data-ttu-id="a0a18-124">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="a0a18-124">Resources</span></span>

-   [<span data-ttu-id="a0a18-125">Поддержка скриптов и шрифтов для Windows</span><span class="sxs-lookup"><span data-stu-id="a0a18-125">Script and Font Support for Windows</span></span>](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [<span data-ttu-id="a0a18-126">Центр разработки Go Global</span><span class="sxs-lookup"><span data-stu-id="a0a18-126">Go Global Development Center</span></span>](https://msdn.microsoft.com/goglobal/default)
-   <span data-ttu-id="a0a18-127">[Отображение и редактирование текста](/previous-versions/windows/apps/hh465442(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="a0a18-127">[Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10))</span></span>
-   [<span data-ttu-id="a0a18-128">Спецификация OpenType</span><span class="sxs-lookup"><span data-stu-id="a0a18-128">OpenType specification</span></span>](https://www.microsoft.com/typography/otspec/)
-   [<span data-ttu-id="a0a18-129">\_ \_ Структура МЕТРИК шрифта дврите</span><span class="sxs-lookup"><span data-stu-id="a0a18-129">DWRITE\_FONT\_METRICS structure</span></span>](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [<span data-ttu-id="a0a18-130">Структура ТЕКСТМЕТРИК</span><span class="sxs-lookup"><span data-stu-id="a0a18-130">TEXTMETRIC Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 