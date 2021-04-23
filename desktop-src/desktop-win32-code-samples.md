---
title: Примеры кода Win32 для классических приложений
description: Сведения о примерах репозиториев для Win32 и способах их поиска.
ms.topic: article
ms.date: 03/19/2021
ms.openlocfilehash: 5a4083697d444f36b31c553a2d6159d4370565d4
ms.sourcegitcommit: 46e75903326c49a6c5cc576ee2b4f67f64a6d5ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105721003"
---
# <a name="desktop-win32-code-samples"></a><span data-ttu-id="c49a7-103">Примеры кода Win32 для классических приложений</span><span class="sxs-lookup"><span data-stu-id="c49a7-103">Desktop Win32 code samples</span></span>

<span data-ttu-id="c49a7-104">См. также [примеры кода](https://developer.microsoft.com/windows/samples/).</span><span class="sxs-lookup"><span data-stu-id="c49a7-104">Also see [Code samples](https://developer.microsoft.com/windows/samples/).</span></span>

## <a name="find-a-sample-for-the-api-youre-interested-in"></a><span data-ttu-id="c49a7-105">Найдите пример для интересующего вас API</span><span class="sxs-lookup"><span data-stu-id="c49a7-105">Find a sample for the API you're interested in</span></span>

<span data-ttu-id="c49a7-106">Microsoft Visual Studio можно использовать для поиска в исходном коде репозитория, чтобы узнать, демонстрируется ли использование определенного API Windows.</span><span class="sxs-lookup"><span data-stu-id="c49a7-106">You can use Microsoft Visual Studio to search an entire repo's source code to see whether the usage of a particular Windows API is being demonstrated.</span></span>

* <span data-ttu-id="c49a7-107">Клонирование любого из репозиториев, перечисленных в следующих разделах (или скачивание ZIP-файла) в локальную файловую систему.</span><span class="sxs-lookup"><span data-stu-id="c49a7-107">Clone any of the repos listed in the sections below (or download the ZIP) to your local file system.</span></span>
* <span data-ttu-id="c49a7-108">Затем **найдите в файле** в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c49a7-108">Then **Find in Files** in Visual Studio.</span></span> <span data-ttu-id="c49a7-109">Установите параметр **Искать в** папке, которую вы клонированы или загрузили, и найдите имя интересующего вас API.</span><span class="sxs-lookup"><span data-stu-id="c49a7-109">Set **Look in** to the folder you cloned or downloaded into, and search for the name of the API you're interested in.</span></span> <span data-ttu-id="c49a7-110">Проверка **совпадения** дает лучшие результаты.</span><span class="sxs-lookup"><span data-stu-id="c49a7-110">Checking **Match case** gives best results.</span></span>
* <span data-ttu-id="c49a7-111">Будьте внимательны при проверке **слова match целиком** , если API можно вызывать в различных &mdash; формах, например **CreateMutex**, **креатемутекса** и **креатемутексв**.</span><span class="sxs-lookup"><span data-stu-id="c49a7-111">Be careful of checking **Match whole word** if the API can be called in various forms&mdash;for example, **CreateMutex**, **CreateMutexA**, and **CreateMutexW**.</span></span> <span data-ttu-id="c49a7-112">В этом случае выполните поиск по слову **CreateMutex** с **полным словом Match** .</span><span class="sxs-lookup"><span data-stu-id="c49a7-112">In that case, search for **CreateMutex** with **Match whole word** unchecked.</span></span>

> [!NOTE]
> <span data-ttu-id="c49a7-113">Вы можете установить [Visual Studio](https://visualstudio.microsoft.com/downloads/) без затрат.</span><span class="sxs-lookup"><span data-stu-id="c49a7-113">You can install [Visual Studio](https://visualstudio.microsoft.com/downloads/) without expense.</span></span> <span data-ttu-id="c49a7-114">Доступен выпуск Community Edition — он предоставляется бесплатно для учащихся, участников проектов с открытым кодом и отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="c49a7-114">A Community edition is available&mdash;it's free for students, open-source contributors, and individuals.</span></span> <span data-ttu-id="c49a7-115">Конечно, вы можете сделать то же самое с любым репозиторием выборок.</span><span class="sxs-lookup"><span data-stu-id="c49a7-115">Of course you can do the same thing with any samples repo.</span></span>

## <a name="the-windows-classic-samples-repo"></a><span data-ttu-id="c49a7-116">Репозиторий с классическими примерами Windows</span><span class="sxs-lookup"><span data-stu-id="c49a7-116">The Windows classic samples repo</span></span>

<span data-ttu-id="c49a7-117">Основной репозиторий, содержащий примеры приложений Windows с помощью API Win32, — это классический репозиторий [примеров Windows](https://github.com/Microsoft/Windows-classic-samples) .</span><span class="sxs-lookup"><span data-stu-id="c49a7-117">The main repo containing sample Windows apps using the Win32 API is the [Windows classic samples](https://github.com/Microsoft/Windows-classic-samples) repo.</span></span>

## <a name="directx-samples"></a><span data-ttu-id="c49a7-118">Примеры DirectX</span><span class="sxs-lookup"><span data-stu-id="c49a7-118">DirectX samples</span></span>

<span data-ttu-id="c49a7-119">Примеры графики DirectX 12, в которых показано, как создавать ресурсоемкие приложения для Windows 10, см. в репозитории [примеров](https://github.com/Microsoft/DirectX-Graphics-Samples) с поддержкой графики DirectX.</span><span class="sxs-lookup"><span data-stu-id="c49a7-119">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="c49a7-120">См. также [примеры DirectX](/windows/uwp/gaming/directx-samples).</span><span class="sxs-lookup"><span data-stu-id="c49a7-120">Also see [DirectX samples](/windows/uwp/gaming/directx-samples).</span></span>

## <a name="older-samples"></a><span data-ttu-id="c49a7-121">Более старые примеры</span><span class="sxs-lookup"><span data-stu-id="c49a7-121">Older samples</span></span>

<span data-ttu-id="c49a7-122">Некоторые старые примеры приложений Win32 можно найти в репозитории [примеров MSDN по коллекции кода](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) .</span><span class="sxs-lookup"><span data-stu-id="c49a7-122">You can find some older Win32 sample apps in the [MSDN Code Gallery Microsoft samples](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) repo.</span></span>

## <a name="see-also"></a><span data-ttu-id="c49a7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c49a7-123">See also</span></span>

* [<span data-ttu-id="c49a7-124">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="c49a7-124">Code samples</span></span>](https://developer.microsoft.com/windows/samples/)
* [<span data-ttu-id="c49a7-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c49a7-125">Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="c49a7-126">Классические примеры Windows</span><span class="sxs-lookup"><span data-stu-id="c49a7-126">Windows classic samples</span></span>](https://github.com/Microsoft/Windows-classic-samples)
* [<span data-ttu-id="c49a7-127">DirectX-Graphics-Samples</span><span class="sxs-lookup"><span data-stu-id="c49a7-127">DirectX-Graphics-Samples</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples)
* [<span data-ttu-id="c49a7-128">Примеры DirectX</span><span class="sxs-lookup"><span data-stu-id="c49a7-128">DirectX samples</span></span>](/windows/uwp/gaming/directx-samples)
* [<span data-ttu-id="c49a7-129">Примеры из коллекции кода MSDN для Microsoft</span><span class="sxs-lookup"><span data-stu-id="c49a7-129">MSDN Code Gallery Microsoft samples</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft)
