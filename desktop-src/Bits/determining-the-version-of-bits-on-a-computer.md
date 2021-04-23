---
title: Определение версии BITS на компьютере
description: Чтобы определить версию BITS на клиентском компьютере, проверьте версию QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773397"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a><span data-ttu-id="3d4cc-103">Определение версии BITS на компьютере</span><span class="sxs-lookup"><span data-stu-id="3d4cc-103">Determining the Version of BITS on a Computer</span></span>

<span data-ttu-id="3d4cc-104">Чтобы определить версию BITS на клиентском компьютере, проверьте версию QMgr.dll.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-104">To determine the version of BITS on the client computer, check the version of QMgr.dll.</span></span> <span data-ttu-id="3d4cc-105">Чтобы найти номер версии библиотеки DLL, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-105">To find the version number of the DLL:</span></span>

-   <span data-ttu-id="3d4cc-106">Обнаружение QMgr.dll в папке% WINDIR% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-106">Locate QMgr.dll in %windir%\\System32.</span></span>
-   <span data-ttu-id="3d4cc-107">Щелкните правой кнопкой мыши QMgr.dll и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-107">Right-click QMgr.dll and click **Properties**.</span></span>
-   <span data-ttu-id="3d4cc-108">Перейдите на вкладку **версия** .</span><span class="sxs-lookup"><span data-stu-id="3d4cc-108">Click the **Version** tab.</span></span>
-   <span data-ttu-id="3d4cc-109">Запишите номер версии.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-109">Note the version number.</span></span>

<span data-ttu-id="3d4cc-110">Для определения версии библиотеки DLL в системе можно также использовать следующий код PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3d4cc-110">You can also use the following PowerShell code to determine the version of the .dll on your system:</span></span>

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

<span data-ttu-id="3d4cc-111">Если библиотека DLL также существует в битах% WINDIR% \\ system32 \\ , повторите предыдущие шаги.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-111">If the DLL also exists in %windir%\\System32\\Bits, repeat the previous steps.</span></span> <span data-ttu-id="3d4cc-112">Служба BITS использует библиотеку DLL с более высоким номером версии.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-112">BITS uses the DLL with the higher version number.</span></span>

<span data-ttu-id="3d4cc-113">В следующей таблице перечислены версии битов и соответствующие номера версий файлов QMgr.dll.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-113">The following table lists the versions of BITS and their corresponding QMgr.dll file version numbers.</span></span>



| <span data-ttu-id="3d4cc-114">Версия BITS</span><span class="sxs-lookup"><span data-stu-id="3d4cc-114">BITS version</span></span> | <span data-ttu-id="3d4cc-115">Номер версии файла QMgr.dll</span><span class="sxs-lookup"><span data-stu-id="3d4cc-115">QMgr.dll file version number</span></span> |
|--------------|------------------------------|
| <span data-ttu-id="3d4cc-116">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="3d4cc-116">BITS 10.1</span></span>    | <span data-ttu-id="3d4cc-117">7,8. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-117">7.8.xxxx.xxxx</span></span>                |
| <span data-ttu-id="3d4cc-118">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-118">BITS 5.0</span></span>     | <span data-ttu-id="3d4cc-119">7.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-119">7.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="3d4cc-120">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-120">BITS 4.0</span></span>     | <span data-ttu-id="3d4cc-121">7,5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-121">7.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="3d4cc-122">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-122">BITS 3.0</span></span>     | <span data-ttu-id="3d4cc-123">7.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-123">7.0.xxxx.xxxx</span></span>                |
| <span data-ttu-id="3d4cc-124">BITS 2,5</span><span class="sxs-lookup"><span data-stu-id="3d4cc-124">BITS 2.5</span></span>     | <span data-ttu-id="3d4cc-125">6.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-125">6.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="3d4cc-126">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-126">BITS 2.0</span></span>     | <span data-ttu-id="3d4cc-127">6,6. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-127">6.6.xxxx.xxxx</span></span>                |
| <span data-ttu-id="3d4cc-128">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="3d4cc-128">BITS 1.5</span></span>     | <span data-ttu-id="3d4cc-129">6.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-129">6.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="3d4cc-130">BITS 1,2</span><span class="sxs-lookup"><span data-stu-id="3d4cc-130">BITS 1.2</span></span>     | <span data-ttu-id="3d4cc-131">6.2. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-131">6.2.xxxx.xxxx</span></span>                |
| <span data-ttu-id="3d4cc-132">BITS 1,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-132">BITS 1.0</span></span>     | <span data-ttu-id="3d4cc-133">6.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="3d4cc-133">6.0.xxxx.xxxx</span></span>                |



 

<span data-ttu-id="3d4cc-134">Кроме того, можно использовать символьные идентификаторы классов для определения версии битов, зарегистрированных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-134">You can also use the symbolic class identifiers to determine the version of BITS that is registered on the computer.</span></span> <span data-ttu-id="3d4cc-135">В следующей таблице перечислены версии битов и соответствующие им символьные идентификаторы классов.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-135">The following table lists the versions of BITS and their corresponding symbolic class identifiers.</span></span> <span data-ttu-id="3d4cc-136">Функция **CoCreateInstance** возвращает **регдб \_ E \_ класснотрег** , если класс не зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="3d4cc-136">The **CoCreateInstance** function returns **REGDB\_E\_CLASSNOTREG** if the class is not registered.</span></span>



| <span data-ttu-id="3d4cc-137">Версия BITS</span><span class="sxs-lookup"><span data-stu-id="3d4cc-137">BITS version</span></span>  | <span data-ttu-id="3d4cc-138">Символьный идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="3d4cc-138">Symbolic class identifier</span></span>         |
|---------------|-----------------------------------|
| <span data-ttu-id="3d4cc-139">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="3d4cc-139">BITS 10.1</span></span>     | <span data-ttu-id="3d4cc-140">CLSID \_ BackgroundCopyManager10 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3d4cc-140">CLSID\_BackgroundCopyManager10\_1</span></span> |
| <span data-ttu-id="3d4cc-141">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-141">BITS 5.0</span></span>      | <span data-ttu-id="3d4cc-142">CLSID \_ BackgroundCopyManager5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-142">CLSID\_BackgroundCopyManager5\_0</span></span>  |
| <span data-ttu-id="3d4cc-143">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-143">BITS 4.0</span></span>      | <span data-ttu-id="3d4cc-144">CLSID \_ BackgroundCopyManager4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-144">CLSID\_BackgroundCopyManager4\_0</span></span>  |
| <span data-ttu-id="3d4cc-145">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-145">BITS 3.0</span></span>      | <span data-ttu-id="3d4cc-146">CLSID \_ BackgroundCopyManager3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-146">CLSID\_BackgroundCopyManager3\_0</span></span>  |
| <span data-ttu-id="3d4cc-147">BITS 2,5</span><span class="sxs-lookup"><span data-stu-id="3d4cc-147">BITS 2.5</span></span>      | <span data-ttu-id="3d4cc-148">CLSID \_ BackgroundCopyManager2 \_ 5</span><span class="sxs-lookup"><span data-stu-id="3d4cc-148">CLSID\_BackgroundCopyManager2\_5</span></span>  |
| <span data-ttu-id="3d4cc-149">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-149">BITS 2.0</span></span>      | <span data-ttu-id="3d4cc-150">CLSID \_ BackgroundCopyManager2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-150">CLSID\_BackgroundCopyManager2\_0</span></span>  |
| <span data-ttu-id="3d4cc-151">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="3d4cc-151">BITS 1.5</span></span>      | <span data-ttu-id="3d4cc-152">CLSID \_ BackgroundCopyManager1 \_ 5</span><span class="sxs-lookup"><span data-stu-id="3d4cc-152">CLSID\_BackgroundCopyManager1\_5</span></span>  |
| <span data-ttu-id="3d4cc-153">BITS 1,2, 1,0</span><span class="sxs-lookup"><span data-stu-id="3d4cc-153">BITS 1.2, 1.0</span></span> | <span data-ttu-id="3d4cc-154">\_БАККГРАУНДКОПИМАНАЖЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="3d4cc-154">CLSID\_BackgroundCopyManager</span></span>      |



 

 

 




