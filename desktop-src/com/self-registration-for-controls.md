---
title: Самостоятельная регистрация для элементов управления
description: Самостоятельная регистрация для элементов управления
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105691674"
---
# <a name="self-registration-for-controls"></a><span data-ttu-id="64a66-103">Самостоятельная регистрация для элементов управления</span><span class="sxs-lookup"><span data-stu-id="64a66-103">Self Registration for Controls</span></span>

<span data-ttu-id="64a66-104">Элементы управления ActiveX должны поддерживать самостоятельную регистрацию, реализуя функции [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) .</span><span class="sxs-lookup"><span data-stu-id="64a66-104">ActiveX controls must support self-registration by implementing the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) functions.</span></span> <span data-ttu-id="64a66-105">Элементы управления ActiveX должны зарегистрировать все стандартные записи реестра для внедряемых объектов и серверов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="64a66-105">ActiveX controls must register all of the standard registry entries for embeddable objects and automation servers.</span></span>

<span data-ttu-id="64a66-106">Элементы управления ActiveX должны использовать API категорий компонентов для регистрации себя в качестве элемента управления и регистрации категорий компонентов, которые требуются для поддержки узла, а также всех категорий, реализуемых элементом управления, в разделе [категории компонентов](component-categories.md).</span><span class="sxs-lookup"><span data-stu-id="64a66-106">ActiveX controls must use the component categories API to register themselves as a control and register the component categories that they require a host to support and any categories that the control implements, see [Component Categories](component-categories.md).</span></span>

<span data-ttu-id="64a66-107">Элементы управления ActiveX также должны зарегистрировать раздел реестра [ToolBoxBitmap32](toolboxbitmap32.md) , хотя это необязательно.</span><span class="sxs-lookup"><span data-stu-id="64a66-107">ActiveX controls should also register the [ToolBoxBitmap32](toolboxbitmap32.md) registry key, although this is not mandatory.</span></span>

<span data-ttu-id="64a66-108">Категория вставляемого компонента должна быть зарегистрирована, только если элемент управления подходит для использования в качестве объекта составного документа.</span><span class="sxs-lookup"><span data-stu-id="64a66-108">The Insertable component category should be registered only if the control is suitable for use as a compound document object.</span></span> <span data-ttu-id="64a66-109">Важно отметить, что объект составного документа должен поддерживать определенные интерфейсы сверх минимально необходимого для элемента управления ActiveX интерфейса [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="64a66-109">It is important to note that a compound document object must support certain interfaces beyond the minimum [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) required for an ActiveX control.</span></span> <span data-ttu-id="64a66-110">Хотя элемент управления ActiveX может быть представлен как объект составного документа, документация по элементу управления должна четко определять, какое поведение следует рассчитывать в этих обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="64a66-110">Although an ActiveX control may qualify as a compound document object, the control's documentation should clearly state what behavior to expect under these circumstances.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64a66-111">См. также</span><span class="sxs-lookup"><span data-stu-id="64a66-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64a66-112">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="64a66-112">Controls</span></span>](controls.md)
</dt> </dl>

 

 