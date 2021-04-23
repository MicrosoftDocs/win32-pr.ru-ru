---
description: Установщик Windows организует установку вокруг концепций компонентов и функций.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Компоненты и компоненты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155139"
---
# <a name="components-and-features"></a><span data-ttu-id="afda9-103">Компоненты и компоненты</span><span class="sxs-lookup"><span data-stu-id="afda9-103">Components and Features</span></span>

<span data-ttu-id="afda9-104">Установщик Windows организует установку вокруг концепций компонентов и функций.</span><span class="sxs-lookup"><span data-stu-id="afda9-104">The Windows Installer organizes an installation around the concepts of components and features.</span></span>

<span data-ttu-id="afda9-105">Функция — это часть общей функциональности приложения, которую пользователь может решить установить независимо.</span><span class="sxs-lookup"><span data-stu-id="afda9-105">A feature is a part of the application's total functionality that a user may decide to install independently.</span></span> <span data-ttu-id="afda9-106">Дополнительные сведения см. в разделе [установщик Windows Features](windows-installer-features.md).</span><span class="sxs-lookup"><span data-stu-id="afda9-106">For more information, see [Windows Installer Features](windows-installer-features.md).</span></span>

<span data-ttu-id="afda9-107">Компонент — это часть приложения или продукта для установки.</span><span class="sxs-lookup"><span data-stu-id="afda9-107">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="afda9-108">Установщик всегда устанавливает или удаляет компонент с компьютера пользователя в качестве согласованного элемента.</span><span class="sxs-lookup"><span data-stu-id="afda9-108">The installer always installs or removes a component from a user's computer as a coherent piece.</span></span> <span data-ttu-id="afda9-109">Компоненты обычно скрываются от пользователя.</span><span class="sxs-lookup"><span data-stu-id="afda9-109">Components are usually hidden from the user.</span></span> <span data-ttu-id="afda9-110">Когда пользователь выбирает компонент для установки, установщик определяет, какие компоненты должны быть установлены для предоставления этой функции.</span><span class="sxs-lookup"><span data-stu-id="afda9-110">When a user selects a feature for installation, the installer determines which components must be installed to provide that feature.</span></span> <span data-ttu-id="afda9-111">Дополнительные сведения см. в разделе [установщик Windows Components](windows-installer-components.md).</span><span class="sxs-lookup"><span data-stu-id="afda9-111">For more information, see [Windows Installer Components](windows-installer-components.md).</span></span>

<span data-ttu-id="afda9-112">Авторы пакетов установки должны решить, как разделить приложение на компоненты и компоненты.</span><span class="sxs-lookup"><span data-stu-id="afda9-112">Authors of installation packages need to decide how to divide their application into features and components.</span></span> <span data-ttu-id="afda9-113">Выбор компонентов в основном определяется функциями приложения с точки зрения пользователя.</span><span class="sxs-lookup"><span data-stu-id="afda9-113">The selection of features is primarily determined by the application's functionality from the user's perspective.</span></span> <span data-ttu-id="afda9-114">Поскольку компоненты обычно должны совместно использоваться несколькими приложениями или даже в разных продуктах, рекомендуется, чтобы авторы были стандартным методом выбора компонентов.</span><span class="sxs-lookup"><span data-stu-id="afda9-114">Because components commonly must be shared across applications, or even across products, it is recommended that authors follow a standard method for selecting components.</span></span> <span data-ttu-id="afda9-115">Дополнительные сведения см. [в разделе Упорядочение приложений по компонентам](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="afda9-115">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

 

 



