---
description: Мситул. MAK — это файл makefile, который можно использовать для создания средств и настраиваемых действий.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Мситул. MAK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156154"
---
# <a name="msitoolmak"></a><span data-ttu-id="2f36f-103">Мситул. MAK</span><span class="sxs-lookup"><span data-stu-id="2f36f-103">Msitool.mak</span></span>

<span data-ttu-id="2f36f-104">Мситул. MAK — это файл makefile, который можно использовать для создания средств и настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="2f36f-104">Msitool.mak is a makefile that you can use to build tools and custom actions.</span></span> <span data-ttu-id="2f36f-105">Его можно использовать с Visual C++ версии 4,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2f36f-105">It may be used with Visual C++ version 4.0 or later.</span></span> <span data-ttu-id="2f36f-106">Дополнительные сведения см. в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="2f36f-106">For more information, see the header file.</span></span> <span data-ttu-id="2f36f-107">Перед включением этого файла необходимо определить набор значений.</span><span class="sxs-lookup"><span data-stu-id="2f36f-107">It requires a set of values to be defined before including this file.</span></span> <span data-ttu-id="2f36f-108">Обычно разработчики размещают их в начале файла. cpp, параметр ifdef должен быть пропущен компилятором C.</span><span class="sxs-lookup"><span data-stu-id="2f36f-108">Typically developers put those at the start of the .cpp, ifdef'd to be skipped by the C compiler.</span></span> <span data-ttu-id="2f36f-109">Аналогичным образом ресурсы добавляются в конец CPP файла.</span><span class="sxs-lookup"><span data-stu-id="2f36f-109">Likewise resources are added to the end of the .cpp file.</span></span> <span data-ttu-id="2f36f-110">Дополнительные сведения см. в разделе Samples.</span><span class="sxs-lookup"><span data-stu-id="2f36f-110">See samples for details.</span></span>

<span data-ttu-id="2f36f-111">ВКБИН можно определить в каталоге, где найдены средства Visual C++ или makefile использует МСВКДИР и МСДЕВДИР.</span><span class="sxs-lookup"><span data-stu-id="2f36f-111">VCBIN can be defined to the directory where the Visual C++ tools are found or the makefile uses MSVCDIR and MSDEVDIR.</span></span> <span data-ttu-id="2f36f-112">Если они не определены, то местоположение не указывается, предполагая, что средства находятся в пути.</span><span class="sxs-lookup"><span data-stu-id="2f36f-112">If those are not defined, it does not specify a location, assuming the tools to be on the PATH.</span></span> <span data-ttu-id="2f36f-113">Ошибка в переменных среды в Visual C++ версии 5,0 заключается в том, что если оба пути не указаны, компоновщику не удается найти Msdis100.dll.</span><span class="sxs-lookup"><span data-stu-id="2f36f-113">An issue with the environment variables in Visual C++ version 5.0 is that if both are not on you path, the linker cannot find Msdis100.dll.</span></span> <span data-ttu-id="2f36f-114">Если скопировать его из МСДЕВДИР в МСВКДИР, он будет работать.</span><span class="sxs-lookup"><span data-stu-id="2f36f-114">If you copy that from MSDEVDIR to MSVCDIR, it works.</span></span> <span data-ttu-id="2f36f-115">Другой вариант — скопировать Msdis100.dll и Rc.exe и Rcdll.dll в МСВКДИР и задать для ВКБИН значение.</span><span class="sxs-lookup"><span data-stu-id="2f36f-115">The other option is to copy Msdis100.dll and Rc.exe and Rcdll.dll to MSVCDIR, and set VCBIN to that.</span></span>

<span data-ttu-id="2f36f-116">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2f36f-116">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f36f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2f36f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f36f-118">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="2f36f-118">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="2f36f-119">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="2f36f-119">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



