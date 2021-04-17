---
description: Рекомендуемый программный метод для установки контекстов в приложении, не поддерживающем рукописный ввод, — использование функций Сетинпутскопе для связывания контекста с полями в приложении.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Настройка контекста с помощью API-интерфейсов Сетинпутскопе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673945"
---
# <a name="setting-context-with-the-setinputscope-apis"></a><span data-ttu-id="f62a4-103">Настройка контекста с помощью API-интерфейсов Сетинпутскопе</span><span class="sxs-lookup"><span data-stu-id="f62a4-103">Setting Context with the SetInputScope APIs</span></span>

<span data-ttu-id="f62a4-104">Рекомендуемый программный метод для установки контекстов в приложении, не поддерживающем рукописный ввод, — использование функций [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) для связывания контекста с полями в приложении.</span><span class="sxs-lookup"><span data-stu-id="f62a4-104">The recommended programmatic technique for setting contexts in an application that is not ink enabled is to use the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions to associate context with the fields in the application.</span></span>

<span data-ttu-id="f62a4-105">Пакет средств разработки Microsoft Windows XP Tablet PC Edition 1,7 был первой версией Microsoft Windows для предложения [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="f62a4-105">The Microsoft Windows XP Tablet PC Edition Development Kit 1.7 was the first version of Microsoft Windows to offer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span> <span data-ttu-id="f62a4-106">Windows Vista также обеспечивает поддержку этих функций.</span><span class="sxs-lookup"><span data-stu-id="f62a4-106">Windows Vista also provides support for these functions.</span></span> <span data-ttu-id="f62a4-107">Определения **сетинпутскопе** объявляются в инпутскопе. idl и инпутскопе. h.</span><span class="sxs-lookup"><span data-stu-id="f62a4-107">The **SetInputScope** definitions are declared in InputScope.idl and InputScope.h.</span></span> <span data-ttu-id="f62a4-108">Дополнительные сведения см. в разделе [Платформа текстовых служб](../tsf/text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="f62a4-108">For more details, see [Text Services Framework](../tsf/text-services-framework.md).</span></span>

<span data-ttu-id="f62a4-109">[**Сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) функции — это рекомендуемый способ задания контекста для элементов управления и приложений, не поддерживающих рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="f62a4-109">The [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions are the recommended way to set context for controls and applications that are not ink enabled.</span></span>

## <a name="common-input-scopes"></a><span data-ttu-id="f62a4-110">Общие области ввода</span><span class="sxs-lookup"><span data-stu-id="f62a4-110">Common Input Scopes</span></span>

<span data-ttu-id="f62a4-111">Используя функции [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) и определенный набор общих областей ввода, описанных в перечислении [**инпутскопе**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , можно улучшить точность распознавания распознавателей рукописного ввода Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f62a4-111">Using the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions and the defined set of common input scopes described in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration, you can improve the recognition accuracy of the Microsoft handwriting recognizers.</span></span>

> [!Note]  
> <span data-ttu-id="f62a4-112">Распознаватели для английского (США), английского (Великобритания), немецкого, французского, итальянского, испанского, нидерландского и португальского языков поддерживают использование общих областей ввода с [**сетинпутскопе**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="f62a4-112">The recognizers for English (United States), English (United Kingdom), German, French, Italian, Spanish, Dutch, and Portuguese currently support using the common input scopes with [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span>

 

 

 
