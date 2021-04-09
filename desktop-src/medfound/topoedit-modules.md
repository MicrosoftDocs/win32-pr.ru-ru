---
description: Модули Топоедит
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Модули Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080571"
---
# <a name="topoedit-modules"></a><span data-ttu-id="f3123-103">Модули Топоедит</span><span class="sxs-lookup"><span data-stu-id="f3123-103">TopoEdit Modules</span></span>

<span data-ttu-id="f3123-104">Средство Топоедит предоставляется с Windows SDK для Windows Server 2008 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f3123-104">The TopoEdit tool is provided with the Windows SDK for Windows Server 2008 and later.</span></span> <span data-ttu-id="f3123-105">Для этого средства требуется Windows Vista или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="f3123-105">The tool requires Windows Vista or later.</span></span>

<span data-ttu-id="f3123-106">Модули Топоедит находятся в папке bin пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="f3123-106">The TopoEdit modules are located in the Bin folder of the SDK.</span></span> <span data-ttu-id="f3123-107">Эти модули:</span><span class="sxs-lookup"><span data-stu-id="f3123-107">These modules are:</span></span>

-   <span data-ttu-id="f3123-108">TopoEdit.exe — исполняемый файл приложения</span><span class="sxs-lookup"><span data-stu-id="f3123-108">TopoEdit.exe—Application executable</span></span>
-   <span data-ttu-id="f3123-109">TEDUTIL.dll — библиотека DLL расширения</span><span class="sxs-lookup"><span data-stu-id="f3123-109">TEDUTIL.dll—Extension DLL</span></span>

<span data-ttu-id="f3123-110">Установка пакета SDK регистрирует библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="f3123-110">The SDK installation registers the DLL.</span></span> <span data-ttu-id="f3123-111">Однако в случае сбоя в командной строке выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="f3123-111">However, if this fails, at a command prompt, run the following.</span></span>


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



<span data-ttu-id="f3123-112">Исходный код для Топоедит также предоставляется в виде образца в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f3123-112">Source code for TopoEdit is also provided as a sample in the Windows SDK.</span></span> <span data-ttu-id="f3123-113">Он находится в следующем каталоге:</span><span class="sxs-lookup"><span data-stu-id="f3123-113">It is located in the following directory:</span></span>

<span data-ttu-id="f3123-114"><samples root>\\Мультимедиа \\ Media Foundation \\ топоедит</span><span class="sxs-lookup"><span data-stu-id="f3123-114"><samples root>\\Multimedia\\Media Foundation\\TopoEdit</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3123-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f3123-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3123-116">Введение в Топоедит</span><span class="sxs-lookup"><span data-stu-id="f3123-116">Introduction to TopoEdit</span></span>](introduction-to-topoedit.md)
</dt> <dt>

[<span data-ttu-id="f3123-117">топоедит</span><span class="sxs-lookup"><span data-stu-id="f3123-117">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



