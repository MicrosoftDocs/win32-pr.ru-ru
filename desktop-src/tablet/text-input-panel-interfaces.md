---
description: В этом разделе содержатся сведения об интерфейсах, используемых для управления внешним видом и поведением панели ввода Tablet PC.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Интерфейсы панели ввода текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272616"
---
# <a name="text-input-panel-interfaces"></a><span data-ttu-id="012dd-103">Интерфейсы панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="012dd-103">Text Input Panel Interfaces</span></span>

<span data-ttu-id="012dd-104">В этом разделе содержатся сведения об интерфейсах, используемых для управления внешним видом и поведением панели ввода Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="012dd-104">This section contains information about the interfaces used to control the appearance and behavior of the Tablet PC Input Panel.</span></span>

> [!Note]  
> <span data-ttu-id="012dd-105">Интерфейсы панели ввода текста не совместимы с автоматизацией.</span><span class="sxs-lookup"><span data-stu-id="012dd-105">The Text Input Panel interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="012dd-106">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="012dd-106">In This Section</span></span>



| <span data-ttu-id="012dd-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="012dd-107">Interface</span></span>                                                                | <span data-ttu-id="012dd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="012dd-108">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="012dd-109">**Интерфейс Ихандвриттентекстинсертион**</span><span class="sxs-lookup"><span data-stu-id="012dd-109">**IHandWrittenTextInsertion Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | <span data-ttu-id="012dd-110">Используется в пользовательском коде ввода текста приложения для вставки текста в текстовое поле и в резервное хранилище текстовых служб.</span><span class="sxs-lookup"><span data-stu-id="012dd-110">Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.</span></span><br/> |
| [<span data-ttu-id="012dd-111">**Интерфейс Итекстинпутпанел**</span><span class="sxs-lookup"><span data-stu-id="012dd-111">**ITextInputPanel Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | <span data-ttu-id="012dd-112">Обеспечивает управление панелью ввода Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="012dd-112">Provides control over the Tablet PC Input Panel.</span></span><br/>                                                                                  |
| [<span data-ttu-id="012dd-113">**Интерфейс Итекстинпутпанелевентсинк**</span><span class="sxs-lookup"><span data-stu-id="012dd-113">**ITextInputPanelEventSink Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | <span data-ttu-id="012dd-114">Определяет методы, обрабатывающие события [**интерфейса итекстинпутпанел**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .</span><span class="sxs-lookup"><span data-stu-id="012dd-114">Defines methods that handle the [**ITextInputPanel Interface**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) events.</span></span><br/>                                      |
| [<span data-ttu-id="012dd-115">**Интерфейс Итекстинпутпанелрунинфо**</span><span class="sxs-lookup"><span data-stu-id="012dd-115">**ITextInputPanelRunInfo Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | <span data-ttu-id="012dd-116">Предоставляет метод, позволяющий определить, выполняется ли в данный момент панель ввода текста.</span><span class="sxs-lookup"><span data-stu-id="012dd-116">Provides a method to determine if the Text Input Panel is currently running.</span></span><br/>                                                      |
| [<span data-ttu-id="012dd-117">**Интерфейс Итипаутокомплетеклиент**</span><span class="sxs-lookup"><span data-stu-id="012dd-117">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)       | <span data-ttu-id="012dd-118">Позволяет клиенту вызывать объект поставщика автоматического завершения для панели ввода текста приложения.</span><span class="sxs-lookup"><span data-stu-id="012dd-118">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="012dd-119">**Интерфейс Итипаутокомплетепровидер**</span><span class="sxs-lookup"><span data-stu-id="012dd-119">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)   | <span data-ttu-id="012dd-120">Управляет стороны приложения для интеграции автоматического завершения автоматической сборки панели ввода текста.</span><span class="sxs-lookup"><span data-stu-id="012dd-120">Manages the application's side of the Text Input Panel auto complete integration.</span></span><br/>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="012dd-121">См. также</span><span class="sxs-lookup"><span data-stu-id="012dd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="012dd-122">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="012dd-122">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




