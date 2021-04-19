---
description: .
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Система свойств Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e96f931d37ef698339f9219a0dc8db43a6003e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692198"
---
# <a name="windows-property-system"></a><span data-ttu-id="763c6-103">Система свойств Windows</span><span class="sxs-lookup"><span data-stu-id="763c6-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="763c6-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="763c6-104">Purpose</span></span>

<span data-ttu-id="763c6-105">Система свойств Windows — это расширяемая система чтения и записи определений данных, которая обеспечивает единообразный способ представления метаданных об элементах оболочки.</span><span class="sxs-lookup"><span data-stu-id="763c6-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="763c6-106">Система свойств Windows в Windows Vista и более поздних версиях позволяет хранить и извлекать метаданные для элементов оболочки.</span><span class="sxs-lookup"><span data-stu-id="763c6-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="763c6-107">Элемент оболочки — это любой отдельный фрагмент содержимого, например файл, папка, электронная почта или контакт.</span><span class="sxs-lookup"><span data-stu-id="763c6-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="763c6-108">Свойство — это отдельный элемент метаданных, связанный с элементом оболочки.</span><span class="sxs-lookup"><span data-stu-id="763c6-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="763c6-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="763c6-109">Developer audience</span></span>

<span data-ttu-id="763c6-110">Прежде чем приступить к ознакомлению с документацией по Windows свойства System SDK, необходимо иметь фундаментальное представление о следующих возможностях.</span><span class="sxs-lookup"><span data-stu-id="763c6-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="763c6-111">Модель COM</span><span class="sxs-lookup"><span data-stu-id="763c6-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="763c6-112">Программирование пространства имен оболочки</span><span class="sxs-lookup"><span data-stu-id="763c6-112">Shell Namespace programming</span></span>

<span data-ttu-id="763c6-113">Общие сведения об COM см. в статье [основы com](../com/com-fundamentals.md).</span><span class="sxs-lookup"><span data-stu-id="763c6-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="763c6-114">Общие сведения о программировании пространства имен оболочки см. в разделе [Начало работы с пространством имен оболочки](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="763c6-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="763c6-115">Сведения об использовании системы свойств Windows см. в разделе [Обзор системы свойств: сценарии разработки](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="763c6-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="763c6-116">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="763c6-116">Run-time requirements</span></span>

<span data-ttu-id="763c6-117">Поддерживаемой средой выполнения для использования системы свойств Windows является Windows Vista или более поздней версии и пакет средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="763c6-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="763c6-118">Windows XP и Microsoft Windows Desktop Search (WDS) 3,0 или более поздней версии также включают подмножество системы свойств Windows.</span><span class="sxs-lookup"><span data-stu-id="763c6-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="763c6-119">Для загрузки Windows 7 или обновления пакета SDK для Windows Vista см. [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="763c6-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="763c6-120">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="763c6-120">In this section</span></span>

-   [<span data-ttu-id="763c6-121">Обзор системы свойств</span><span class="sxs-lookup"><span data-stu-id="763c6-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="763c6-122">Руководством разработчика системы свойств Windows</span><span class="sxs-lookup"><span data-stu-id="763c6-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="763c6-123">Справочник по свойствам системы</span><span class="sxs-lookup"><span data-stu-id="763c6-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="763c6-124">Образцы кода системы свойств</span><span class="sxs-lookup"><span data-stu-id="763c6-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
