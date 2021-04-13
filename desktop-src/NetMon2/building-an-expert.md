---
description: В этом разделе описывается создание обобщенного эксперта, поставляемого с пакетом SDK для сетевой монитор.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Создание эксперта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264371"
---
# <a name="building-an-expert"></a><span data-ttu-id="6ab84-103">Создание эксперта</span><span class="sxs-lookup"><span data-stu-id="6ab84-103">Building an Expert</span></span>

<span data-ttu-id="6ab84-104">В этом разделе описывается создание обобщенного эксперта, поставляемого с пакетом SDK для сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="6ab84-104">This topic describes how to build a generic expert that ships with the Network Monitor SDK.</span></span>

> [!Note]  
> <span data-ttu-id="6ab84-105">Перед созданием следующих примеров кода установите пакет SDK для сетевой монитор и инициализируйте файл MySetEnv.bat.</span><span class="sxs-lookup"><span data-stu-id="6ab84-105">Before creating the following code examples, install the Network Monitor SDK and initialize the MySetEnv.bat file.</span></span>

 

<span data-ttu-id="6ab84-106">**Создание общего эксперта**</span><span class="sxs-lookup"><span data-stu-id="6ab84-106">**To build a generic expert**</span></span>

1.  <span data-ttu-id="6ab84-107">Откройте командную строку сетевой монитор и перейдите в \\ подкаталог экспертов, например C: \\ Program Files \\ NetMonSDK2 \\ экспертов.</span><span class="sxs-lookup"><span data-stu-id="6ab84-107">Open a Network Monitor command prompt and navigate to the \\Experts subdirectory; for example, C:\\Program Files\\NetMonSDK2\\Experts.</span></span>
2.  <span data-ttu-id="6ab84-108">Введите команду **xcopy/e/s/V Блрплате мексперт**; Затем при появлении запроса введите **D**.</span><span class="sxs-lookup"><span data-stu-id="6ab84-108">Type **xcopy /e /s /v Blrplate MyExpert**; then, when prompted, type **D**.</span></span>
3.  <span data-ttu-id="6ab84-109">Перейдите в \\ подкаталог мексперт.</span><span class="sxs-lookup"><span data-stu-id="6ab84-109">Move to the \\MyExpert subdirectory.</span></span>
4.  <span data-ttu-id="6ab84-110">Введите **ren блрплате \* . \* Мексперт \* . \***</span><span class="sxs-lookup"><span data-stu-id="6ab84-110">Type **ren Blrplate\*.\* MyExpert\*.\***.</span></span> <span data-ttu-id="6ab84-111">Убедитесь, что все файлы должным образом переименованы.</span><span class="sxs-lookup"><span data-stu-id="6ab84-111">Ensure that all files are properly renamed.</span></span> <span data-ttu-id="6ab84-112">Проверьте имена файлов, сравнив файлы в \\ \\ подкаталоге экспертов блрплате.</span><span class="sxs-lookup"><span data-stu-id="6ab84-112">Verify the file names by comparing the files in the \\Experts\\Blrplate subdirectory.</span></span>
5.  <span data-ttu-id="6ab84-113">Измените файл makefile, заменив все вхождения **блрплате** на **мексперт**.</span><span class="sxs-lookup"><span data-stu-id="6ab84-113">Edit the Makefile by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
6.  <span data-ttu-id="6ab84-114">Измените оба файла. cpp, заменив все вхождения **блрплате** на **мексперт**.</span><span class="sxs-lookup"><span data-stu-id="6ab84-114">Edit both .cpp files by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span> <span data-ttu-id="6ab84-115">Имейте в виду, что идентификатор диалогового окна в файле config. cpp должен быть прописной буквой (например, **мексперт**).</span><span class="sxs-lookup"><span data-stu-id="6ab84-115">Be aware that the dialog box identifier in Config.cpp must be capitalized (for example, **MYEXPERT**).</span></span>
7.  <span data-ttu-id="6ab84-116">Измените Мексперт. h, заменив все вхождения **блрплате** на **мексперт**.</span><span class="sxs-lookup"><span data-stu-id="6ab84-116">Edit MyExpert.h by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
8.  <span data-ttu-id="6ab84-117">Измените Resrc1. h, переименовав **блрплате** в **мексперт**.</span><span class="sxs-lookup"><span data-stu-id="6ab84-117">Edit Resrc1.h by renaming **BLRPLATE** to **MYEXPERT**.</span></span> <span data-ttu-id="6ab84-118">(Помните, что **мексперт** должны быть прописными буквами).</span><span class="sxs-lookup"><span data-stu-id="6ab84-118">(Remember, **MYEXPERT** must be capitalized).</span></span>
9.  <span data-ttu-id="6ab84-119">Измените файл Мексперт. RC, переименовав **\_ \_ \_ диалоговое окно Идд блрплате config** в **\_ \_ \_ диалоговое окно Идд мексперт config**.</span><span class="sxs-lookup"><span data-stu-id="6ab84-119">Edit the MyExpert.rc file by renaming **IDD\_BLRPLATE\_CONFIG\_DIALOG** to **IDD\_MYEXPERT\_CONFIG\_DIALOG**.</span></span>
10. <span data-ttu-id="6ab84-120">Введите **NMAKE** , чтобы создать DLL-файл.</span><span class="sxs-lookup"><span data-stu-id="6ab84-120">Type **nmake** to build the DLL file.</span></span> <span data-ttu-id="6ab84-121">Чтобы проверить сборку, измените каталог на \\ подкаталог obj и убедитесь, что файл существует.</span><span class="sxs-lookup"><span data-stu-id="6ab84-121">To verify the build, change directory to the \\Obj subdirectory and verify that the file exists.</span></span> <span data-ttu-id="6ab84-122">Дополнительные сведения см. в разделе [Просмотр свойств DLL эксперта](viewing-expert-dll-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6ab84-122">For more information, see [Viewing Expert DLL Properties](viewing-expert-dll-properties.md).</span></span>

<span data-ttu-id="6ab84-123">После завершения сборки вы получите файл DLL эксперта, который можно тестировать и развертывать с помощью сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="6ab84-123">When the build is complete, you will have an expert DLL that you can test and deploy with Network Monitor.</span></span> <span data-ttu-id="6ab84-124">Дополнительные сведения об установке эксперта см. [в статье Установка эксперта в сетевой монитор 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="6ab84-124">For more information about installing an expert, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span> <span data-ttu-id="6ab84-125">Дополнительные сведения об отладке эксперта см. [в разделе Отладка эксперта](debugging-an-expert.md).</span><span class="sxs-lookup"><span data-stu-id="6ab84-125">For more information about debugging an expert, see [Debugging an Expert](debugging-an-expert.md).</span></span>

 

 



