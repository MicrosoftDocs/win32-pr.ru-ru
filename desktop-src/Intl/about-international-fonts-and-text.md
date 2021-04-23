---
description: В подразделах этого раздела рассматриваются основные функциональные возможности международных шрифтов.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Управление международными шрифтами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ade599577f97c696d3205e32bfaaca106ddaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683739"
---
# <a name="international-font-management"></a><span data-ttu-id="8de6c-103">Управление международными шрифтами</span><span class="sxs-lookup"><span data-stu-id="8de6c-103">International Font Management</span></span>

<span data-ttu-id="8de6c-104">В подразделах этого раздела рассматриваются основные функциональные возможности международных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="8de6c-104">The topics in this section address the basic functionality of International Fonts.</span></span> <span data-ttu-id="8de6c-105">Инструкции по использованию международных шрифтов в приложениях см. в статье [перечисление и выбор шрифтов для разных языков](using-international-fonts-and-text.md) и [использование MS Shell Dlg и MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).</span><span class="sxs-lookup"><span data-stu-id="8de6c-105">For instructions on using the international font technology in your applications, see [International Font Enumeration and Selection](using-international-fonts-and-text.md) and [Using MS Shell Dlg and MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).</span></span>

## <a name="font-management-infrastructure"></a><span data-ttu-id="8de6c-106">Инфраструктура управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="8de6c-106">Font Management Infrastructure</span></span>

<span data-ttu-id="8de6c-107">Начиная с Windows 7, инфраструктура управления шрифтами поддерживает скрытие шрифтов, которые не подходят для списков выбора шрифта пользователем.</span><span class="sxs-lookup"><span data-stu-id="8de6c-107">Starting with Windows 7, the font management infrastructure supports the hiding of fonts which are not appropriate for a user's font selection lists.</span></span> <span data-ttu-id="8de6c-108">Параметры системы по умолчанию автоматически скрывают шрифты, которые не предназначены для языков ввода (клавиатуры), включенных в системе ОС.</span><span class="sxs-lookup"><span data-stu-id="8de6c-108">The default system settings will choose to auto-hide fonts which are not designed for the input language(s) (keyboards) enabled on the OS system.</span></span> <span data-ttu-id="8de6c-109">Кроме того, пользователи могут вручную скрыть шрифты на панели управления "шрифты".</span><span class="sxs-lookup"><span data-stu-id="8de6c-109">In addition, users can choose to manually hide fonts in the Fonts Control Panel.</span></span> <span data-ttu-id="8de6c-110">Эта функция означает, что пользователям больше не придется столкнуться с длинными списками недопустимых шрифтов и особенно важны для международных пользователей, работающих в сценариях, не являющихся восточноазиатскими.</span><span class="sxs-lookup"><span data-stu-id="8de6c-110">This feature means users need no longer be faced with long lists of inappropriate fonts, and is particularly valuable for international users working in non-Latin scripts.</span></span>

<span data-ttu-id="8de6c-111">В Windows 7 нет интерфейсов API для непосредственного запроса того, какие шрифты скрыты, или для настройки скрытых шрифтов.</span><span class="sxs-lookup"><span data-stu-id="8de6c-111">In Windows 7, there are no APIs for directly querying which fonts are hidden, or for setting fonts to be hidden.</span></span> <span data-ttu-id="8de6c-112">Однако это не значит, что вы не можете воспользоваться этой функцией в вашем приложении.</span><span class="sxs-lookup"><span data-stu-id="8de6c-112">However, this does not mean you cannot take advantage of this feature in your application.</span></span> <span data-ttu-id="8de6c-113">Если вы используете Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) API (общий диалог шрифтов) для включения выбора шрифта сегодня, вы получите новое поведение бесплатно.</span><span class="sxs-lookup"><span data-stu-id="8de6c-113">If you use the Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) API (Font common dialog) to enable font selection today, you will get the new behavior for free.</span></span> <span data-ttu-id="8de6c-114">Новая лента Windows Scenic (элементы управления шрифтом), появившаяся в Windows 7, также поддерживает это поведение и предоставляет еще одну причину "Риббонизе" ваших приложений.</span><span class="sxs-lookup"><span data-stu-id="8de6c-114">The new Windows Scenic Ribbon (Font Controls) introduced in Windows 7 also supports this behavior and provides another reason to "Ribbonize" your applications.</span></span> <span data-ttu-id="8de6c-115">Дополнительные сведения об использовании элементов управления шрифтом на ленте и **ChooseFont** для вывода шрифтов при фильтрации скрытых шрифтов см. в статье [перечисление международного шрифта и выбор](using-international-fonts-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="8de6c-115">For details of using Font Controls in Ribbon and **ChooseFont** to display fonts while filtering out the hidden fonts, please reference [International Font Enumeration and Selection](using-international-fonts-and-text.md).</span></span>

<span data-ttu-id="8de6c-116">Обратите внимание, что скрытие шрифтов влияет только на пользовательский интерфейс выбора шрифта.</span><span class="sxs-lookup"><span data-stu-id="8de6c-116">Note that hiding fonts only impacts font selection UI.</span></span> <span data-ttu-id="8de6c-117">Он не влияет на API-интерфейсы рисования.</span><span class="sxs-lookup"><span data-stu-id="8de6c-117">It does not impact drawing APIs.</span></span> <span data-ttu-id="8de6c-118">Когда шрифт выбирается в контексте устройства, он не влияет на прорисовку из-за скрытого шрифта.</span><span class="sxs-lookup"><span data-stu-id="8de6c-118">When a font is selected into a device context, there is no effect on drawing due to the font being hidden.</span></span> <span data-ttu-id="8de6c-119">Функция [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) продолжит перечислять шрифты, для которых задано значение Hidden.</span><span class="sxs-lookup"><span data-stu-id="8de6c-119">The [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) function continues to enumerate fonts that are set to hidden.</span></span>

## <a name="gdi-font-embedding-and-subsetting"></a><span data-ttu-id="8de6c-120">Встраивание и поднастройка шрифта GDI</span><span class="sxs-lookup"><span data-stu-id="8de6c-120">GDI Font Embedding and Subsetting</span></span>

<span data-ttu-id="8de6c-121">Технология международных шрифтов использует библиотеку служб внедрения шрифтов, которая позволяет объединять шрифты TrueType и OpenType в документ или файл.</span><span class="sxs-lookup"><span data-stu-id="8de6c-121">International Fonts technology makes use of the Font Embedding Services Library to allow you to bundle TrueType and OpenType fonts into a document or file.</span></span> <span data-ttu-id="8de6c-122">Встраивание шрифта в файл гарантирует, что этот шрифт будет присутствовать на компьютере, получающем файл.</span><span class="sxs-lookup"><span data-stu-id="8de6c-122">Embedding a font in a file guarantees that the font will be present on the computer receiving the file.</span></span> <span data-ttu-id="8de6c-123">Дополнительные сведения см. в разделе [Справочник по внедрению шрифтов](../gdi/font-embedding-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8de6c-123">For more information, see [Font Embedding Reference](../gdi/font-embedding-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8de6c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="8de6c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de6c-125">Перечисление международных шрифтов и выбор</span><span class="sxs-lookup"><span data-stu-id="8de6c-125">International Font Enumeration and Selection</span></span>](using-international-fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="8de6c-126">Использование MS Shell Dlg и MS Shell Dlg 2</span><span class="sxs-lookup"><span data-stu-id="8de6c-126">Using MS Shell Dlg and MS Shell Dlg 2</span></span>](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[<span data-ttu-id="8de6c-127">Справочник по внедрению шрифтов</span><span class="sxs-lookup"><span data-stu-id="8de6c-127">Font Embedding Reference</span></span>](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
