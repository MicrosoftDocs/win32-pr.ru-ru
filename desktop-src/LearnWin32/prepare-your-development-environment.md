---
title: Подготовка среды разработки
description: Подготовка среды разработки
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337204"
---
# <a name="prepare-your-development-environment"></a><span data-ttu-id="e62a0-103">Подготовка среды разработки</span><span class="sxs-lookup"><span data-stu-id="e62a0-103">Prepare Your Development Environment</span></span>

<span data-ttu-id="e62a0-104">Для написания программы Windows на C или C++ необходимо установить пакет средств разработки программного обеспечения (SDK) для Microsoft Windows или Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e62a0-104">To write a Windows program in C or C++, you must install the Microsoft Windows Software Development Kit (SDK) or Microsoft Visual Studio.</span></span> <span data-ttu-id="e62a0-105">Windows SDK содержит заголовки и библиотеки, необходимые для компиляции и связывания приложения.</span><span class="sxs-lookup"><span data-stu-id="e62a0-105">The Windows SDK contains the headers and libraries necessary to compile and link your application.</span></span> <span data-ttu-id="e62a0-106">Windows SDK также содержит программы командной строки для создания приложений Windows, включая компилятор Visual C++ и компоновщик.</span><span class="sxs-lookup"><span data-stu-id="e62a0-106">The Windows SDK also contains command-line tools for building Windows applications, including the Visual C++ compiler and linker.</span></span> <span data-ttu-id="e62a0-107">Хотя вы можете компилировать и создавать программы Windows с помощью программ командной строки, рекомендуется использовать Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e62a0-107">Although you can compile and build Windows programs with the command-line tools, we recommend using Microsoft Visual Studio.</span></span> <span data-ttu-id="e62a0-108">Скачать бесплатную версию Visual Studio Community или бесплатные пробные версии Visual Studio можно [здесь](https://visualstudio.microsoft.com/downloads/).</span><span class="sxs-lookup"><span data-stu-id="e62a0-108">You can download a free download of Visual Studio Community or free trials of other versions of Visual Studio [here](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="e62a0-109">Каждый выпуск Windows SDK предназначен для последней версии Windows, а также для нескольких предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="e62a0-109">Each release of the Windows SDK targets the latest version of Windows as well as several previous versions.</span></span> <span data-ttu-id="e62a0-110">В заметках о выпуске перечислены поддерживаемые платформы, но если вы не обслуживаете приложение для очень старой версии Windows, следует установить последнюю версию Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e62a0-110">The release notes list the specific platforms that are supported, but unless you are maintaining an application for a very old version of Windows, you should install the latest release of the Windows SDK.</span></span> <span data-ttu-id="e62a0-111">Последнюю Windows SDK можно скачать [здесь](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="e62a0-111">You can download the latest Windows SDK [here](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="e62a0-112">Windows SDK поддерживает разработку как 32-разрядных, так и 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="e62a0-112">The Windows SDK supports development of both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="e62a0-113">Интерфейсы API Windows спроектированы таким образом, чтобы один и тот же код можно было компилировать для 32-или 64-бит без изменений.</span><span class="sxs-lookup"><span data-stu-id="e62a0-113">The Windows APIs are designed so that the same code can compile for 32-bit or 64-bit without changes.</span></span>

> [!Note]  
> <span data-ttu-id="e62a0-114">Windows SDK не поддерживает разработку драйверов оборудования, и эта серия не будет обсуждать разработку драйверов.</span><span class="sxs-lookup"><span data-stu-id="e62a0-114">The Windows SDK does not support hardware driver development, and this series will not discuss driver development.</span></span> <span data-ttu-id="e62a0-115">Сведения о создании драйвера оборудования см. в разделе [Начало работы с драйверами Windows](/windows-hardware/drivers/gettingstarted/).</span><span class="sxs-lookup"><span data-stu-id="e62a0-115">For information about writing a hardware driver, see [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).</span></span>

## <a name="next"></a><span data-ttu-id="e62a0-116">Следующая</span><span class="sxs-lookup"><span data-stu-id="e62a0-116">Next</span></span>

[<span data-ttu-id="e62a0-117">Соглашения о написании кода Windows</span><span class="sxs-lookup"><span data-stu-id="e62a0-117">Windows Coding Conventions</span></span>](windows-coding-conventions.md)

## <a name="related-topics"></a><span data-ttu-id="e62a0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e62a0-118">Related topics</span></span>

* [<span data-ttu-id="e62a0-119">Скачать Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="e62a0-119">Download Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="e62a0-120">Скачать Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e62a0-120">Download Windows SDK</span></span>](https://developer.microsoft.com/windows/downloads/windows-10-sdk)