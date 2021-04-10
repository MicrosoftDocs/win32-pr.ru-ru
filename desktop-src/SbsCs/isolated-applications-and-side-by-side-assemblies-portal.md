---
description: Управление совместной работой сборок и версиями библиотек DLL в системах, размещенных в параллельном хранилище сборок, из программ. Создавайте манифесты сборок и сами описания приложений для совместного использования сборок и перенаправления библиотек DLL.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Изолированные приложения и параллельные сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144509"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="94d5d-104">Изолированные приложения и параллельные сборки</span><span class="sxs-lookup"><span data-stu-id="94d5d-104">Isolated Applications and Side-by-side Assemblies</span></span>

## <a name="purpose"></a><span data-ttu-id="94d5d-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="94d5d-105">Purpose</span></span>

<span data-ttu-id="94d5d-106">Изолированные приложения и параллельные сборки — это решение Microsoft Windows, уменьшающее конфликты управления версиями в клиентских приложениях Windows.</span><span class="sxs-lookup"><span data-stu-id="94d5d-106">Isolated Applications and Side-by-side Assemblies is a Microsoft Windows solution that reduces versioning conflicts in Windows-client applications.</span></span> <span data-ttu-id="94d5d-107">В Windows разработчики приложений могут создавать изолированные приложения, которые полностью описывают и не затрагивают изменения в реестре, других приложениях или других версиях сборок, работающих в системе.</span><span class="sxs-lookup"><span data-stu-id="94d5d-107">With Windows, application developers can build isolated applications that are fully self-describing and unaffected by changes to the registry, other applications, or other versions of assemblies running on the system.</span></span> <span data-ttu-id="94d5d-108">Авторы и администраторы приложений могут использовать манифесты для управления совместным использованием параллельных сборок после развертывания на глобальном уровне или на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="94d5d-108">Application authors and administrators can use manifests to manage the sharing of side-by-side assemblies after deployment on either a global or per-application basis.</span></span> <span data-ttu-id="94d5d-109">Клиенты получают преимущества от изолированных приложений, которые более стабильны и надежно обновляются.</span><span class="sxs-lookup"><span data-stu-id="94d5d-109">Customers benefit from isolated applications that are more stable and more reliably updated.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="94d5d-110">Где применимо</span><span class="sxs-lookup"><span data-stu-id="94d5d-110">Where applicable</span></span>

<span data-ttu-id="94d5d-111">Изолированные приложения и параллельный доступ к сборкам можно использовать для разработки приложений, которые безопасно совместно используют сборки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="94d5d-111">Isolated applications and side-by-side assembly sharing can be used to develop applications that safely share operating system assemblies.</span></span> <span data-ttu-id="94d5d-112">Разработчики могут использовать эту технологию для исправления конфликтов управления версиями библиотек DLL, вызванных несовместимой версией общей сборки.</span><span class="sxs-lookup"><span data-stu-id="94d5d-112">Developers can use this technology to correct DLL versioning conflicts caused by an incompatible version of a shared assembly.</span></span>

<span data-ttu-id="94d5d-113">Если приложение должно постоянно получать версию тестируемого компонента, можно изолировать приложение таким образом, чтобы оно всегда выполнялось с проверенной версией компонента на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="94d5d-113">If your application must consistently get the version of a component you have tested, it is possible to isolate your application so that it will always be run with the tested version of the component on the user's computer.</span></span>

<span data-ttu-id="94d5d-114">Изолированные приложения и параллельные сборки предназначены для разработки приложений в стиле рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="94d5d-114">Isolated Applications and Side-by-side Assemblies is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="94d5d-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="94d5d-115">Developer audience</span></span>

<span data-ttu-id="94d5d-116">Эта документация в основном предназначена для разработчиков программного обеспечения, разработчиков приложений и сетевых администраторов.</span><span class="sxs-lookup"><span data-stu-id="94d5d-116">This documentation is primarily intended for software developers, application developers, and network administrators:</span></span>

-   <span data-ttu-id="94d5d-117">Разработчики программного обеспечения, желающие создать изолированные приложения, которые будут использовать параллельные сборки, предоставляемые корпорацией Майкрософт и другими издателями параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="94d5d-117">Software developers who want to create isolated applications that will use the side-by-side assemblies made available by Microsoft and other side-by-side assembly publishers.</span></span>
-   <span data-ttu-id="94d5d-118">Разработчики приложений, заинтересованные в создании собственных параллельных сборок для изоляции своих приложений.</span><span class="sxs-lookup"><span data-stu-id="94d5d-118">Application developers who are interested in creating their own side-by-side assemblies to isolate their applications.</span></span>
-   <span data-ttu-id="94d5d-119">Сетевые администраторы, которым требуются дополнительные сведения об изолированных приложениях.</span><span class="sxs-lookup"><span data-stu-id="94d5d-119">Network administrators who want more information about isolated applications.</span></span>

<span data-ttu-id="94d5d-120">В качестве основной ссылки для параллельного совместного использования сборок и изолированных приложений эта документация содержит общие фундаментальные сведения о создании манифестов и параллельных сборок, установке изолированных приложений и параллельных сборок, а также об использовании API контекста активации.</span><span class="sxs-lookup"><span data-stu-id="94d5d-120">As the primary reference for side-by-side assembly sharing and isolated applications, this documentation provides general background information about authoring manifests and side-by-side assemblies, installing isolated applications and side-by-side assemblies, and using the Activation Context API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="94d5d-121">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="94d5d-121">Run-time requirements</span></span>

<span data-ttu-id="94d5d-122">В Windows Server 2003 и более поздних версиях или Windows XP и более поздних версиях требуется использовать параллельные сборки и манифесты для изоляции приложений и использования API контекста активации.</span><span class="sxs-lookup"><span data-stu-id="94d5d-122">Windows Server 2003 and later or Windows XP and later is required to use side-by-side assemblies and manifests to isolate applications and to use the Activation Context API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="94d5d-123">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="94d5d-123">In this section</span></span>



| <span data-ttu-id="94d5d-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="94d5d-124">Topic</span></span>                                                         | <span data-ttu-id="94d5d-125">Описание</span><span class="sxs-lookup"><span data-stu-id="94d5d-125">Description</span></span>                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="94d5d-126">Ссылки</span><span class="sxs-lookup"><span data-stu-id="94d5d-126">Reference</span></span>](side-by-side-assemblies-reference.md)<br/> | <span data-ttu-id="94d5d-127">Документация по изолированным приложениям и параллельным сборкам.</span><span class="sxs-lookup"><span data-stu-id="94d5d-127">Documentation of Isolated Applications and Side-by-side Assemblies.</span></span><br/> |



 

 

 




