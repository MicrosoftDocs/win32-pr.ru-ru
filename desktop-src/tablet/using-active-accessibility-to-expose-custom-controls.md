---
description: Описание использования Active Accessibility для предоставления пользовательских элементов управления для планшетных ПК.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Использование Active Accessibility для предоставления настраиваемых элементов управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701452"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a><span data-ttu-id="06a50-103">Использование Active Accessibility для предоставления настраиваемых элементов управления</span><span class="sxs-lookup"><span data-stu-id="06a50-103">Using Active Accessibility to Expose Custom Controls</span></span>

<span data-ttu-id="06a50-104">Active Accessibility Майкрософт можно использовать как эффективный способ обеспечения совместимости пользовательских элементов управления с вспомогательными средствами.</span><span class="sxs-lookup"><span data-stu-id="06a50-104">You can use Microsoft Active Accessibility as an effective way to make custom controls compatible with accessibility aids.</span></span> <span data-ttu-id="06a50-105">Для Active Accessibility требуется, чтобы приложение:</span><span class="sxs-lookup"><span data-stu-id="06a50-105">Active Accessibility requires that the application:</span></span>

-   <span data-ttu-id="06a50-106">Создание объектов модели COM, представляющих отдельные пользовательские элементы управления или группы элементов управления, которые должны поддерживать интерфейс **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="06a50-106">Create Component Object Model (COM) objects that represent individual custom controls or groups of controls that properly support the **IAccessible** interface.</span></span> <span data-ttu-id="06a50-107">(Объект может быть создан по запросу, когда запрос запрашивается клиентом Active Accessibility.)</span><span class="sxs-lookup"><span data-stu-id="06a50-107">(The object may be created on demand when it is requested by an Active Accessibility client.)</span></span>
-   <span data-ttu-id="06a50-108">Вызывайте [**нотифивиневент**](/windows/win32/api/winuser/nf-winuser-notifywinevent) , когда элементы управления создаются или уничтожаются, получают или теряют фокус или иным образом меняют состояние.</span><span class="sxs-lookup"><span data-stu-id="06a50-108">Call [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) when the controls are created or destroyed, gain or lose focus, or otherwise change state.</span></span>
-   <span data-ttu-id="06a50-109">Обрабатывайте \_ сообщение WM GetObject при использовании для запроса свойств объекта или объектов.</span><span class="sxs-lookup"><span data-stu-id="06a50-109">Handle the WM\_GETOBJECT message when used to query properties of the object or objects.</span></span>

<span data-ttu-id="06a50-110">В этом обсуждении окно, содержащее другие пользовательские объекты, также должно быть предоставлено Active Accessibility, что позволяет клиенту обнаруживать дочерние объекты и переходить к ним.</span><span class="sxs-lookup"><span data-stu-id="06a50-110">For the purposes of this discussion, a window containing other custom objects also needs to be exposed to Active Accessibility, allowing the client to discover and navigate to the child objects.</span></span> <span data-ttu-id="06a50-111">Дополнительные сведения о том, как сделать пользовательские элементы управления совместимыми с вспомогательными средствами, см. в разделе [Специальные возможности](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="06a50-111">For more information about how to make custom controls compatible with accessibility aids, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
