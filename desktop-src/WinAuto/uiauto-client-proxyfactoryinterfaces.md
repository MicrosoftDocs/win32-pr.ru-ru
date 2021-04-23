---
title: Интерфейсы фабрики прокси-серверов для клиентов
description: В этом разделе описываются интерфейсы фабрики прокси для неуправляемых клиентских приложений автоматизации пользовательского интерфейса.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068470"
---
# <a name="proxy-factory-interfaces-for-clients"></a><span data-ttu-id="05212-103">Интерфейсы фабрики прокси-серверов для клиентов</span><span class="sxs-lookup"><span data-stu-id="05212-103">Proxy Factory Interfaces for Clients</span></span>

<span data-ttu-id="05212-104">В этом разделе описываются интерфейсы фабрики прокси для неуправляемых клиентских приложений автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="05212-104">This section describes the proxy factory interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="05212-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="05212-105">In this section</span></span>



| <span data-ttu-id="05212-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="05212-106">Interface</span></span>                                                                                      | <span data-ttu-id="05212-107">Описание</span><span class="sxs-lookup"><span data-stu-id="05212-107">Description</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05212-108">**иуиаутоматионпроксифактори**</span><span class="sxs-lookup"><span data-stu-id="05212-108">**IUIAutomationProxyFactory**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | <span data-ttu-id="05212-109">Предоставляет свойства и методы объекта, который создает поставщик автоматизации ПОЛЬЗОВАТЕЛЬСКОГО интерфейса Майкрософт для элементов пользовательского интерфейса, не имеющих встроенной поддержки модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="05212-109">Exposes properties and methods of an object that creates a Microsoft UI Automation provider for UI elements that do not have native support for UI Automation.</span></span> <span data-ttu-id="05212-110">Этот интерфейс реализуется прокси-серверами.</span><span class="sxs-lookup"><span data-stu-id="05212-110">This interface is implemented by proxies.</span></span><br/>                                                                          |
| [<span data-ttu-id="05212-111">**иуиаутоматионпроксифакторентри**</span><span class="sxs-lookup"><span data-stu-id="05212-111">**IUIAutomationProxyFactoryEntry**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | <span data-ttu-id="05212-112">Представляет фабрику прокси в таблице, поддерживаемой автоматизацией пользовательского интерфейса, и предоставляет свойства и методы, которые могут использоваться клиентскими приложениями для взаимодействия с объектами [**иуиаутоматионпроксифактори**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .</span><span class="sxs-lookup"><span data-stu-id="05212-112">Represents a proxy factory in the table maintained by UI Automation, and exposes properties and methods that can be used by client applications to interact with [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) objects.</span></span><br/>                                   |
| [<span data-ttu-id="05212-113">**иуиаутоматионпроксифакторимаппинг**</span><span class="sxs-lookup"><span data-stu-id="05212-113">**IUIAutomationProxyFactoryMapping**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | <span data-ttu-id="05212-114">Предоставляет свойства и методы для таблицы фабрик прокси-серверов.</span><span class="sxs-lookup"><span data-stu-id="05212-114">Exposes properties and methods for a table of proxy factories.</span></span> <span data-ttu-id="05212-115">Каждая запись таблицы представлена интерфейсом [**иуиаутоматионпроксифакторентри**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) .</span><span class="sxs-lookup"><span data-stu-id="05212-115">Each table entry is represented by an [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) interface.</span></span> <span data-ttu-id="05212-116">Записи находятся в том порядке, в котором система будет пытаться использовать прокси-серверы.</span><span class="sxs-lookup"><span data-stu-id="05212-116">The entries are in the order in which the system will attempt to use the proxies.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="05212-117">См. также</span><span class="sxs-lookup"><span data-stu-id="05212-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05212-118">Клиенты автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="05212-118">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





