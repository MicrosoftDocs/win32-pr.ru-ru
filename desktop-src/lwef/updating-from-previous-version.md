---
title: Обновление с предыдущей версии
description: Обновление с предыдущей версии
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691152"
---
# <a name="updating-from-previous-version"></a><span data-ttu-id="d5bf0-103">Обновление с предыдущей версии</span><span class="sxs-lookup"><span data-stu-id="d5bf0-103">Updating from Previous Version</span></span>

<span data-ttu-id="d5bf0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d5bf0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d5bf0-105">Приложения, созданные и скомпилированные с помощью предыдущей версии 1,5 агента Microsoft Agent, должны работать без изменений в новой версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-105">Applications built and compiled with the previous 1.5 version of Microsoft Agent should run without modification under the new 2.0 version.</span></span> <span data-ttu-id="d5bf0-106">Свойству [**Connected**](connected-property.md) больше не может быть присвоено значение **false**; Некоторые свойства объекта Спичинпут, которые были заменены, все еще существуют, но больше не включают значения, а сервер больше не запускает события [**перезапуска**](https://www.bing.com/search?q=**Restart**) и [**завершения работы**](https://www.bing.com/search?q=**Shutdown**) .</span><span class="sxs-lookup"><span data-stu-id="d5bf0-106">The [**Connected**](connected-property.md) property can no longer be set to **False**; certain properties of the SpeechInput object that have been replaced still exist, but no longer turn any values, and the server no longer fires the [**Restart**](https://www.bing.com/search?q=**Restart**) and [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) events.</span></span>

<span data-ttu-id="d5bf0-107">Однако при обновлении приложений для использования элемента управления агента 2,0 может потребоваться изменить код.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-107">However, if you update your applications to use the Agent 2.0 control, you may have to modify your code.</span></span> <span data-ttu-id="d5bf0-108">Если вы установили версию 2,0 Microsoft Agent и загрузили проект Visual Basic использовать более раннюю версию элемента управления агента, Visual Basic включает параметр, который автоматически отображает сообщение о том, что обнаружена новая версия элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-108">If you have installed the 2.0 version of Microsoft Agent and load a Visual Basic project use the earlier version of the Agent control, Visual Basic includes an option that will automatically display a message indicating that it detected a new version of the control.</span></span> <span data-ttu-id="d5bf0-109">Чтобы обеспечить правильную работу приложения, всегда выбирайте более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-109">To ensure proper operation of your application, always choose to use the later version.</span></span>

<span data-ttu-id="d5bf0-110">Для других языков программирования (например, Microsoft Office 97 VBA) для обновления элемента управления может потребоваться сначала удалить элемент управления агента 1,5 и сохранить код.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-110">For other programming languages (such as Microsoft Office 97 VBA), to update the control, you may have to first remove the 1.5 Agent control and save your code.</span></span> <span data-ttu-id="d5bf0-111">Затем закройте среду программирования, перезапустите среду программирования, перезагрузите код и вставьте новый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-111">Then, quit the programming environment, restart the programming environment, reload your code and insert the new control.</span></span> <span data-ttu-id="d5bf0-112">Избегайте редактирования приложения с поддержкой агента 2,0 в том же экземпляре среды программирования, в которой вы редактируете приложение с поддержкой агента 1,5 в.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-112">Avoid editing an Agent 2.0-enabled application in the same instance of the programming environment that you are editing an Agent 1.5-enabled application in.</span></span> <span data-ttu-id="d5bf0-113">Некоторые среды программирования могут не справиться с различиями между двумя версиями элементов управления.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-113">Some programming environments may not handle the differences between the two versions of controls.</span></span>

<span data-ttu-id="d5bf0-114">После установки выпуска Agent 2,0 вы сможете удалить выпуск агента 1,5 в системе.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-114">You should be able to uninstall the Agent 1.5 release on your system after installing the Agent 2.0 release.</span></span> <span data-ttu-id="d5bf0-115">Однако если агент 1,5 установлен в выпуске 2,0, может потребоваться переустановить 2,0.</span><span class="sxs-lookup"><span data-stu-id="d5bf0-115">However, if Agent 1.5 is installed over the 2.0 release, you may have to reinstall 2.0.</span></span>

 

 




