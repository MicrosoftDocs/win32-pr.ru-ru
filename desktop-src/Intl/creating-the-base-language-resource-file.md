---
description: Создание файла ресурсов базового языка
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Создание файла ресурсов базового языка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081402"
---
# <a name="creating-the-base-language-resource-file"></a><span data-ttu-id="e2105-103">Создание файла ресурсов базового языка</span><span class="sxs-lookup"><span data-stu-id="e2105-103">Creating the Base Language Resource File</span></span>

<span data-ttu-id="e2105-104">Ресурсы для элементов пользовательского интерфейса определяются на базовом языке, поддерживаемом приложением, например на английском (США).</span><span class="sxs-lookup"><span data-stu-id="e2105-104">Resources for user interface elements are defined for the basic language that the application supports, for example, English (United States).</span></span> <span data-ttu-id="e2105-105">Примером файла ресурсов Win32 PE является RC-файл, созданный с помощью компилятора RC.</span><span class="sxs-lookup"><span data-stu-id="e2105-105">An example of a Win32 PE resource file is an .rc file, created using RC Compiler.</span></span> <span data-ttu-id="e2105-106">Дополнительные сведения о создании RC-файла см. в разделе [о файлах ресурсов](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="e2105-106">For details of .rc file creation, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="e2105-107">При использовании RC-файла для базовых ресурсов языка вы можете использовать файл конфигурации ресурса для представления данных конфигурации ресурсов в формате XML.</span><span class="sxs-lookup"><span data-stu-id="e2105-107">If using an .rc file for the base language resources, you have the option of using a resource configuration file for an XML representation of resource configuration data.</span></span> <span data-ttu-id="e2105-108">Сведения о создании этого файла см. в разделе [Подготовка файла конфигурации ресурса](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="e2105-108">To create this file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="e2105-109">Для определения ресурсов базового языка можно также использовать PE-файл, отличный от Win32.</span><span class="sxs-lookup"><span data-stu-id="e2105-109">You can also use a non-Win32 PE file to define base language resources.</span></span> <span data-ttu-id="e2105-110">Например, для этой цели можно использовать файл. XML или. txt.</span><span class="sxs-lookup"><span data-stu-id="e2105-110">For example, you might use an .xml file or .txt file for this purpose.</span></span>

> [!Note]  
> <span data-ttu-id="e2105-111">При определении ресурсов базового языка с помощью PE-файла, отличного от Win32, нельзя использовать компилятор RC для определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="e2105-111">When you define base language resources using a non-Win32 PE file, you cannot use RC Compiler for resource definition.</span></span> <span data-ttu-id="e2105-112">Вместо этого определите собственный формат ресурсов, и ваше приложение должно предоставить собственные функции для поиска и загрузки необходимых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2105-112">Instead, you define your own resource format, and your application must provide its own functionality to find and load the required resources.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e2105-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e2105-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2105-114">Подготовка ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2105-114">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="e2105-115">Подготовка файла конфигурации ресурса</span><span class="sxs-lookup"><span data-stu-id="e2105-115">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
