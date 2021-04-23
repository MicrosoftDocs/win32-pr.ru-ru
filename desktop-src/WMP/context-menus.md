---
title: Контекстные меню
description: Контекстные меню
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Интернет-магазины проигрывателя Windows Media, контекстные меню
- Интернет-магазины, контекстные меню
- Тип 1 Интернет-магазины, контекстные меню
- Интернет-магазины проигрывателя Windows Media, Настраиваемые контекстные меню
- Интернет-магазины, Настраиваемые контекстные меню
- Тип 1 Интернет-магазины, Настраиваемые контекстные меню
- контекстные меню
- настраиваемые контекстных меню
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412479"
---
# <a name="context-menus"></a><span data-ttu-id="00ed1-111">Контекстные меню</span><span class="sxs-lookup"><span data-stu-id="00ed1-111">Context Menus</span></span>

<span data-ttu-id="00ed1-112">Интернет-магазины могут предоставлять настраиваемые контекстные меню.</span><span class="sxs-lookup"><span data-stu-id="00ed1-112">Online stores can provide custom context menus.</span></span> <span data-ttu-id="00ed1-113">Для этого подключаемый модуль интернет-магазина реализует метод [ивмпконтентпартнер::-Commands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) .</span><span class="sxs-lookup"><span data-stu-id="00ed1-113">To do this, the online store plug-in implements the [IWMPContentPartner::GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) method.</span></span> <span data-ttu-id="00ed1-114">Проигрыватель Windows Media вызывает этот метод для предоставления сведений о расположении в пользовательском интерфейсе, в котором отображается контекстное меню (где пользователь щелкнул правой кнопкой мыши).</span><span class="sxs-lookup"><span data-stu-id="00ed1-114">Windows Media Player calls this method to provide information about the location in the user interface where the context menu is displayed (where the user right-clicked).</span></span> <span data-ttu-id="00ed1-115">Подключаемый модуль возвращает массив структур [вмпконтекстменуинфо](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) , описывающих каждый пункт контекстного меню, включая идентификатор команды для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="00ed1-115">The plug-in returns an array of [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) structures that describe each context menu item, including a command ID for each.</span></span>

<span data-ttu-id="00ed1-116">Когда проигрыватель Windows Media извлекает массив, проигрыватель использует массив для создания контекстного меню, которое видит пользователь.</span><span class="sxs-lookup"><span data-stu-id="00ed1-116">After Windows Media Player has retrieved the array, the Player uses the array to build the context menu the user sees.</span></span> <span data-ttu-id="00ed1-117">Когда пользователь щелкает элемент в контекстном меню, игрок вызывает [ивмпконтентпартнер:: инвокекомманд](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), передавая идентификатор команды, связанный с пунктом меню, через параметр *двкоммандид* .</span><span class="sxs-lookup"><span data-stu-id="00ed1-117">When the user clicks an item in the context menu, the Player calls [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passing the command ID associated with the menu item through the *dwCommandID* parameter.</span></span> <span data-ttu-id="00ed1-118">Проигрыватель также передает значение расположения библиотеки и массив идентификаторов, представляющих элементы, которые были вызваны меню, например массив идентификаторов Track.</span><span class="sxs-lookup"><span data-stu-id="00ed1-118">The Player also passes a library location value and an array of IDs that represents the items the menu was invoked upon, such as an array of track IDs.</span></span> <span data-ttu-id="00ed1-119">С помощью этих сведений подключаемый модуль может запускать любой соответствующий процесс в ответ на щелчок пользователя.</span><span class="sxs-lookup"><span data-stu-id="00ed1-119">By using this information, the plug-in can start any appropriate process in response to the user's mouse click.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00ed1-120">См. также</span><span class="sxs-lookup"><span data-stu-id="00ed1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ed1-121">**Сведения об Интернет-магазинах типа 1**</span><span class="sxs-lookup"><span data-stu-id="00ed1-121">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




