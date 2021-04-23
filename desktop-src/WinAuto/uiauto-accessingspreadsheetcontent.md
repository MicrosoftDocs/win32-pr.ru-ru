---
title: Доступ к содержимому электронной таблицы
description: В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт могут получать доступ к содержимому электронной таблицы.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- Клиенты, доступ к содержимому электронной таблицы
- Клиенты, текстовые элементы управления
- Клиенты, шаблон элемента управления электронной таблицы
- Клиенты, шаблон элемента управления Спреадшититем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31495086614f34aeff378a8565200fa03f2dad62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338937"
---
# <a name="accessing-spreadsheet-content"></a><span data-ttu-id="44c1e-107">Доступ к содержимому электронной таблицы</span><span class="sxs-lookup"><span data-stu-id="44c1e-107">Accessing Spreadsheet Content</span></span>

<span data-ttu-id="44c1e-108">Текстовый элемент управления, содержащий электронную таблицу, может обеспечить клиентам доступ к содержимому, поддерживая шаблоны элементов управления [электронной таблицы](uiauto-implementingspreadsheet.md) и [спреадшититем](uiauto-implementingspreadsheetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="44c1e-108">A text-based control that contains spreadsheet content can enable clients to access the content by supporting the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns.</span></span> <span data-ttu-id="44c1e-109">В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт могут получать доступ к содержимому электронной таблицы.</span><span class="sxs-lookup"><span data-stu-id="44c1e-109">This topic describes how Microsoft UI Automation client applications can access the content of a spreadsheet.</span></span>

<span data-ttu-id="44c1e-110">Чтобы определить, поддерживает ли текстовый элемент управления [электронную таблицу](uiauto-implementingspreadsheet.md) и шаблоны элементов управления [спреадшититем](uiauto-implementingspreadsheetitem.md) , сначала извлеките интерфейс [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) для элемента управления (см. раздел [Получение элементов модели автоматизации пользовательского интерфейса](uiauto-obtainingelements.md)). Затем вызовите метод [**иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , указав идентификатор шаблона элемента управления [**UIA \_ спреадшитпаттернид**](uiauto-controlpattern-ids.md) или [**UIA \_ спреадшититемпаттернид**](uiauto-controlpattern-ids.md), и вариант, который получает значение true, если элемент управления поддерживает определенный шаблон элемента управления.</span><span class="sxs-lookup"><span data-stu-id="44c1e-110">To determine whether a text-based control supports the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns, first retrieve the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the control (see [Obtaining UI Automation Elements](uiauto-obtainingelements.md).) Next, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying a control pattern identifier of [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) or [**UIA\_SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md), and a variant that receives TRUE if the control supports the particular control pattern.</span></span>

<span data-ttu-id="44c1e-111">Чтобы получить доступ к содержимому таблицы, извлеките интерфейс [**иуиаутоматионспреадшитпаттерн**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) , вызвав метод [**Иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) и указав [**UIA \_ спреадшитпаттернид**](uiauto-controlpattern-ids.md) в качестве идентификатора шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="44c1e-111">To access the spreadsheet content, retrieve the [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) interface by calling [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method and specifying [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) as the control pattern identifier.</span></span> <span data-ttu-id="44c1e-112">Затем используйте метод [**иуиаутоматионспреадшитпаттерн:: жетитембинаме**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) , чтобы получить интерфейс [**иуиаутоматионспреадшититем**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) для определенного элемента электронной таблицы (обычно это ячейка).</span><span class="sxs-lookup"><span data-stu-id="44c1e-112">Next, use the [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) method to get the [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) interface for a particular spreadsheet item (typically a cell).</span></span> <span data-ttu-id="44c1e-113">Используйте свойства и методы интерфейса **иуиаутоматионспреадшититем** , чтобы получить формулу для ячейки и все заметки, связанные с ячейкой.</span><span class="sxs-lookup"><span data-stu-id="44c1e-113">Use the properties and methods of the **IUIAutomationSpreadsheetItem** interface to retrieve the formula for the cell, and any annotations associated with the cell.</span></span> <span data-ttu-id="44c1e-114">Дополнительные сведения о заметках см [. в разделе Получение заметок.](uiauto-usingtextrangeobjects.md)</span><span class="sxs-lookup"><span data-stu-id="44c1e-114">For more information about annotations, see [Retrieving Annotations.](uiauto-usingtextrangeobjects.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="44c1e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="44c1e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c1e-116">Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого</span><span class="sxs-lookup"><span data-stu-id="44c1e-116">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="44c1e-117">Работа с элементами управления на основе текста</span><span class="sxs-lookup"><span data-stu-id="44c1e-117">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 