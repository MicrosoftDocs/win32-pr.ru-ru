---
description: Система свойств Windows
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Система свойств Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49e44c988d3a91572be1b42d5fbaf75e664d7f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089882"
---
# <a name="windows-property-system"></a><span data-ttu-id="584be-103">Система свойств Windows</span><span class="sxs-lookup"><span data-stu-id="584be-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="584be-104">Цель</span><span class="sxs-lookup"><span data-stu-id="584be-104">Purpose</span></span>

<span data-ttu-id="584be-105">Система свойств Windows — это расширяемая система чтения и записи определений данных, которая обеспечивает единообразный способ представления метаданных об элементах оболочки.</span><span class="sxs-lookup"><span data-stu-id="584be-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="584be-106">Система свойств Windows в Windows Vista и более поздних версиях позволяет хранить и извлекать метаданные для элементов оболочки.</span><span class="sxs-lookup"><span data-stu-id="584be-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="584be-107">Элемент оболочки — это любой отдельный фрагмент содержимого, например файл, папка, электронная почта или контакт.</span><span class="sxs-lookup"><span data-stu-id="584be-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="584be-108">Свойство — это отдельный элемент метаданных, связанный с элементом оболочки.</span><span class="sxs-lookup"><span data-stu-id="584be-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="584be-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="584be-109">Developer audience</span></span>

<span data-ttu-id="584be-110">Прежде чем приступить к ознакомлению с документацией по Windows свойства System SDK, необходимо иметь фундаментальное представление о следующих возможностях.</span><span class="sxs-lookup"><span data-stu-id="584be-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="584be-111">Модель COM</span><span class="sxs-lookup"><span data-stu-id="584be-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="584be-112">Программирование пространства имен оболочки</span><span class="sxs-lookup"><span data-stu-id="584be-112">Shell Namespace programming</span></span>

<span data-ttu-id="584be-113">Общие сведения об COM см. в статье [основы com](../com/com-fundamentals.md).</span><span class="sxs-lookup"><span data-stu-id="584be-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="584be-114">Общие сведения о программировании пространства имен оболочки см. в разделе [Начало работы с пространством имен оболочки](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="584be-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="584be-115">Сведения об использовании системы свойств Windows см. в разделе [Обзор системы свойств: сценарии разработки](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="584be-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="584be-116">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="584be-116">Run-time requirements</span></span>

<span data-ttu-id="584be-117">Поддерживаемой средой выполнения для использования системы свойств Windows является Windows Vista или более поздней версии и пакет средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="584be-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="584be-118">Windows XP и Microsoft Windows Desktop Search (WDS) 3,0 или более поздней версии также включают подмножество системы свойств Windows.</span><span class="sxs-lookup"><span data-stu-id="584be-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="584be-119">Для загрузки Windows 7 или обновления пакета SDK для Windows Vista см. [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="584be-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="584be-120">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="584be-120">In this section</span></span>

-   [<span data-ttu-id="584be-121">Обзор системы свойств</span><span class="sxs-lookup"><span data-stu-id="584be-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="584be-122">Руководством разработчика системы свойств Windows</span><span class="sxs-lookup"><span data-stu-id="584be-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="584be-123">Справочник по свойствам системы</span><span class="sxs-lookup"><span data-stu-id="584be-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="584be-124">Образцы кода системы свойств</span><span class="sxs-lookup"><span data-stu-id="584be-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
