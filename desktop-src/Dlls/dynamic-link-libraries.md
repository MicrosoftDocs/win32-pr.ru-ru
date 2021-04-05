---
description: Библиотека динамической компоновки (DLL) — это модуль, который содержит функции и данные, которые могут использоваться другим модулем (приложением или библиотекой DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Библиотеки Dynamic-Link (библиотеки динамической компоновки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811488"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a><span data-ttu-id="ccb2b-103">Библиотеки Dynamic-Link (библиотеки динамической компоновки)</span><span class="sxs-lookup"><span data-stu-id="ccb2b-103">Dynamic-Link Libraries (Dynamic-Link Libraries)</span></span>

<span data-ttu-id="ccb2b-104">*Библиотека динамической компоновки* (DLL) — это модуль, который содержит функции и данные, которые могут использоваться другим модулем (приложением или библиотекой DLL).</span><span class="sxs-lookup"><span data-stu-id="ccb2b-104">A *dynamic-link library* (DLL) is a module that contains functions and data that can be used by another module (application or DLL).</span></span>

<span data-ttu-id="ccb2b-105">Библиотека DLL может определять два вида функций: экспортированные и внутренние.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-105">A DLL can define two kinds of functions: exported and internal.</span></span> <span data-ttu-id="ccb2b-106">Экспортированные функции предназначены для вызова другими модулями, а также из библиотеки DLL, в которой они определены.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-106">The exported functions are intended to be called by other modules, as well as from within the DLL where they are defined.</span></span> <span data-ttu-id="ccb2b-107">Внутренние функции обычно предназначены для вызова только из библиотеки DLL, в которой они определены.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-107">Internal functions are typically intended to be called only from within the DLL where they are defined.</span></span> <span data-ttu-id="ccb2b-108">Хотя библиотека DLL может экспортировать данные, ее данные обычно используются только ее функциями.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-108">Although a DLL can export data, its data is generally used only by its functions.</span></span> <span data-ttu-id="ccb2b-109">Однако нет ничего, чтобы предотвратить чтение или запись этого адреса другим модулем.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-109">However, there is nothing to prevent another module from reading or writing that address.</span></span>

<span data-ttu-id="ccb2b-110">Библиотеки DLL позволяют разделения приложения таким образом, чтобы их функциональность можно было обновлять и многократно использовать.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-110">DLLs provide a way to modularize applications so that their functionality can be updated and reused more easily.</span></span> <span data-ttu-id="ccb2b-111">Библиотеки DLL также помогают сократить нагрузку на память, когда несколько приложений используют одни и те же функции одновременно, поскольку хотя каждое приложение получает собственную копию данных библиотеки DLL, приложения совместно используют код библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-111">DLLs also help reduce memory overhead when several applications use the same functionality at the same time, because although each application receives its own copy of the DLL data, the applications share the DLL code.</span></span>

<span data-ttu-id="ccb2b-112">Прикладной программный интерфейс (API) Windows реализуется как набор библиотек DLL, поэтому любой процесс, использующий API Windows, использует динамическую компоновку.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-112">The Windows application programming interface (API) is implemented as a set of DLLs, so any process that uses the Windows API uses dynamic linking.</span></span>

-   [<span data-ttu-id="ccb2b-113">Сведения о библиотеках Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="ccb2b-113">About Dynamic-Link Libraries</span></span>](about-dynamic-link-libraries.md)
-   [<span data-ttu-id="ccb2b-114">Использование библиотек Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="ccb2b-114">Using Dynamic-Link Libraries</span></span>](using-dynamic-link-libraries.md)
-   [<span data-ttu-id="ccb2b-115">Ссылка на библиотеку динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="ccb2b-115">Dynamic-Link Library Reference</span></span>](dynamic-link-library-reference.md)

> [!Note]  
> <span data-ttu-id="ccb2b-116">Если пользователь испытывает трудности с библиотекой DLL на компьютере, обратитесь в службу поддержки клиентов для поставщика программного обеспечения, который публикует библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="ccb2b-116">If you are a user experiencing difficulty with a DLL on your computer, you should contact customer support for the software vendor that publishes the DLL.</span></span> <span data-ttu-id="ccb2b-117">Если вы считаете, что вам нужна поддержка продуктов Майкрософт (включая Windows), перейдите на наш сайт технической поддержки по адресу [support.Microsoft.com](https://support.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ccb2b-117">If you feel you are in need of support for a Microsoft product (including Windows), please go to our technical support site at [support.microsoft.com](https://support.microsoft.com).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ccb2b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ccb2b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccb2b-119">Библиотеки DLL (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="ccb2b-119">DLLs (Visual C++)</span></span>](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
