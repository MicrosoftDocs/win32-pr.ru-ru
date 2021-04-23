---
description: Создание приложений DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Создание приложений DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672933"
---
# <a name="building-directshow-applications"></a><span data-ttu-id="b33f6-103">Создание приложений DirectShow</span><span class="sxs-lookup"><span data-stu-id="b33f6-103">Building DirectShow Applications</span></span>

<span data-ttu-id="b33f6-104">В этом разделе описываются заголовки и библиотеки, необходимые для создания приложений DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b33f6-104">This topic describes the headers and libraries needed to build DirectShow applications.</span></span>

<span data-ttu-id="b33f6-105">В [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx)доступны последние заголовки и библиотеки DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b33f6-105">The latest DirectShow headers and libraries are available in the [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span></span>

## <a name="header-files"></a><span data-ttu-id="b33f6-106">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b33f6-106">Header Files</span></span>

<span data-ttu-id="b33f6-107">Все приложения DirectShow используют файл заголовка, показанный в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b33f6-107">All DirectShow applications use the header file shown in the following table.</span></span>



| <span data-ttu-id="b33f6-108">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="b33f6-108">Header File</span></span> | <span data-ttu-id="b33f6-109">Требуется для</span><span class="sxs-lookup"><span data-stu-id="b33f6-109">Required For</span></span>                 |
|-------------|------------------------------|
| <span data-ttu-id="b33f6-110">DShow. h</span><span class="sxs-lookup"><span data-stu-id="b33f6-110">Dshow.h</span></span>     | <span data-ttu-id="b33f6-111">Все приложения DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b33f6-111">All DirectShow applications.</span></span> |



 

<span data-ttu-id="b33f6-112">Для некоторых интерфейсов DirectShow требуются дополнительные файлы заголовков.</span><span class="sxs-lookup"><span data-stu-id="b33f6-112">Some DirectShow interfaces require additional header files.</span></span> <span data-ttu-id="b33f6-113">Эти требования указаны в справочнике по интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="b33f6-113">These requirements are noted in the interface reference.</span></span>

## <a name="library-files"></a><span data-ttu-id="b33f6-114">Файлы библиотек</span><span class="sxs-lookup"><span data-stu-id="b33f6-114">Library Files</span></span>

<span data-ttu-id="b33f6-115">DirectShow использует статические файлы библиотек, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b33f6-115">DirectShow uses the static library files shown in the following table.</span></span>



| <span data-ttu-id="b33f6-116">Файл библиотеки</span><span class="sxs-lookup"><span data-stu-id="b33f6-116">Library File</span></span> | <span data-ttu-id="b33f6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b33f6-117">Description</span></span>                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b33f6-118">Стрмиидс. lib</span><span class="sxs-lookup"><span data-stu-id="b33f6-118">Strmiids.lib</span></span> | <span data-ttu-id="b33f6-119">Экспортирует идентификаторы классов (CLSID) и идентификаторы интерфейса (идентификаторов IID).</span><span class="sxs-lookup"><span data-stu-id="b33f6-119">Exports class identifiers (CLSIDs) and interface identifiers (IIDs).</span></span>                                                           |
| <span data-ttu-id="b33f6-120">Quartz. lib</span><span class="sxs-lookup"><span data-stu-id="b33f6-120">Quartz.lib</span></span>   | <span data-ttu-id="b33f6-121">Экспортирует функцию [**амжетеррортекст**](/windows/win32/api/errors/nf-errors-amgeterrortexta) .</span><span class="sxs-lookup"><span data-stu-id="b33f6-121">Exports the [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) function.</span></span> <span data-ttu-id="b33f6-122">Если не вызвать эту функцию, эта библиотека не требуется.</span><span class="sxs-lookup"><span data-stu-id="b33f6-122">If you do not call this function, this library is not required.</span></span> |



 

<span data-ttu-id="b33f6-123">Используйте одинаковые lib файлы для сборок отладки и выпуска.</span><span class="sxs-lookup"><span data-stu-id="b33f6-123">Use the same .lib files for debug and release builds.</span></span>

## <a name="filter-base-classes"></a><span data-ttu-id="b33f6-124">Фильтровать базовые классы</span><span class="sxs-lookup"><span data-stu-id="b33f6-124">Filter Base Classes</span></span>

<span data-ttu-id="b33f6-125">Windows SDK предоставляет набор классов C++, рекомендуемых при написании настраиваемого фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b33f6-125">The Windows SDK provides a set of C++ classes that are recommended if you are writing a custom DirectShow filter.</span></span> <span data-ttu-id="b33f6-126">Эти классы предоставляются в виде образца кода, который можно скомпилировать в статическую библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b33f6-126">These classes are provided as sample code, which you can compile to a static library.</span></span> <span data-ttu-id="b33f6-127">Дополнительные сведения см. в разделе [базовые классы DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b33f6-127">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="redistributable-dlls"></a><span data-ttu-id="b33f6-128">Распространяемые библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="b33f6-128">Redistributable DLLs</span></span>

<span data-ttu-id="b33f6-129">Приложения DirectShow, написанные для Windows XP с пакетом обновления 2 (SP2) и более поздних версий, не требуют повторного распространения DLL-библиотек DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b33f6-129">DirectShow applications written for Windows XP with Service Pack 2 (SP2) and later do not need to redistribute any DirectShow DLLs.</span></span>

<span data-ttu-id="b33f6-130">Для Windows XP с пакетом обновления 1 (SP1) и более ранних версий распространяемые DLL-библиотеки DirectShow доступны в пакете SDK для Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="b33f6-130">For Windows XP with Service Pack 1 (SP1) and earlier, redistributable DirectShow DLLs are available from the Microsoft DirectX SDK.</span></span> <span data-ttu-id="b33f6-131">Последняя версия этих библиотек DLL — версия 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="b33f6-131">The latest version of these DLLs is version 9.0c.</span></span> <span data-ttu-id="b33f6-132">Дальнейшая разработка распространяемых библиотек DLL не планируется.</span><span class="sxs-lookup"><span data-stu-id="b33f6-132">No further development of these redistributable DLLs is planned.</span></span> <span data-ttu-id="b33f6-133">Windows XP с пакетом обновления 2 (SP2) содержит библиотеки DLL версии 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="b33f6-133">Windows XP with Service Pack 2 (SP2) contains the version 9.0c DLLs.</span></span>

<span data-ttu-id="b33f6-134">Пакеты редстрибутабле содержат следующие библиотеки DLL:</span><span class="sxs-lookup"><span data-stu-id="b33f6-134">The redstributable packages contain the following DLLs:</span></span>

-   <span data-ttu-id="b33f6-135">dxnt.cab</span><span class="sxs-lookup"><span data-stu-id="b33f6-135">dxnt.cab</span></span>
    -   <span data-ttu-id="b33f6-136">amstream.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-136">amstream.dll</span></span>
    -   <span data-ttu-id="b33f6-137">devenum.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-137">devenum.dll</span></span>
    -   <span data-ttu-id="b33f6-138">encapi.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-138">encapi.dll</span></span>
    -   <span data-ttu-id="b33f6-139">ks.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-139">ks.sys</span></span>
    -   <span data-ttu-id="b33f6-140">ksolay.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-140">ksolay.ax</span></span>
    -   <span data-ttu-id="b33f6-141">ksproxy.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-141">ksproxy.ax</span></span>
    -   <span data-ttu-id="b33f6-142">ksuser.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-142">ksuser.dll</span></span>
    -   <span data-ttu-id="b33f6-143">l3codecx.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-143">l3codecx.ax</span></span>
    -   <span data-ttu-id="b33f6-144">mciqtz32.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-144">mciqtz32.dll</span></span>
    -   <span data-ttu-id="b33f6-145">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-145">mpg2splt.ax</span></span>
    -   <span data-ttu-id="b33f6-146">msdmo.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-146">msdmo.dll</span></span>
    -   <span data-ttu-id="b33f6-147">mskssrv.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-147">mskssrv.sys</span></span>
    -   <span data-ttu-id="b33f6-148">mspclock.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-148">mspclock.sys</span></span>
    -   <span data-ttu-id="b33f6-149">mspqm.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-149">mspqm.sys</span></span>
    -   <span data-ttu-id="b33f6-150">mstee.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-150">mstee.sys</span></span>
    -   <span data-ttu-id="b33f6-151">mswebdvd.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-151">mswebdvd.dll</span></span>
    -   <span data-ttu-id="b33f6-152">qasf.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-152">qasf.dll</span></span>
    -   <span data-ttu-id="b33f6-153">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-153">qcap.dll</span></span>
    -   <span data-ttu-id="b33f6-154">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-154">qdv.dll</span></span>
    -   <span data-ttu-id="b33f6-155">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-155">qdvd.dll</span></span>
    -   <span data-ttu-id="b33f6-156">qedit.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-156">qedit.dll</span></span>
    -   <span data-ttu-id="b33f6-157">qedwipes.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-157">qedwipes.dll</span></span>
    -   <span data-ttu-id="b33f6-158">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-158">quartz.dll</span></span>
    -   <span data-ttu-id="b33f6-159">stream.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-159">stream.sys</span></span>
    -   <span data-ttu-id="b33f6-160">swenum.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-160">swenum.sys</span></span>
-   <span data-ttu-id="b33f6-161">bda.cab</span><span class="sxs-lookup"><span data-stu-id="b33f6-161">bda.cab</span></span>
    -   <span data-ttu-id="b33f6-162">bdaplgin.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-162">bdaplgin.ax</span></span>
    -   <span data-ttu-id="b33f6-163">bdasup.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-163">bdasup.sys</span></span>
    -   <span data-ttu-id="b33f6-164">ccdecode.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-164">ccdecode.sys</span></span>
    -   <span data-ttu-id="b33f6-165">ipsink.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-165">ipsink.ax</span></span>
    -   <span data-ttu-id="b33f6-166">kstvtune.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-166">kstvtune.ax</span></span>
    -   <span data-ttu-id="b33f6-167">kswdmcap.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-167">kswdmcap.ax</span></span>
    -   <span data-ttu-id="b33f6-168">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-168">ksxbar.ax</span></span>
    -   <span data-ttu-id="b33f6-169">mpe.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-169">mpe.sys</span></span>
    -   <span data-ttu-id="b33f6-170">mpeg2data.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-170">mpeg2data.ax</span></span>
    -   <span data-ttu-id="b33f6-171">msdv.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-171">msdv.sys</span></span>
    -   <span data-ttu-id="b33f6-172">msdvbnp.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-172">msdvbnp.ax</span></span>
    -   <span data-ttu-id="b33f6-173">msvidctl.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-173">msvidctl.dll</span></span>
    -   <span data-ttu-id="b33f6-174">msyuv.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-174">msyuv.dll</span></span>
    -   <span data-ttu-id="b33f6-175">nabtsfec.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-175">nabtsfec.sys</span></span>
    -   <span data-ttu-id="b33f6-176">ndisip.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-176">ndisip.sys</span></span>
    -   <span data-ttu-id="b33f6-177">psisdecd.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-177">psisdecd.dll</span></span>
    -   <span data-ttu-id="b33f6-178">psisrndr.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-178">psisrndr.ax</span></span>
    -   <span data-ttu-id="b33f6-179">slip.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-179">slip.sys</span></span>
    -   <span data-ttu-id="b33f6-180">streamip.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-180">streamip.sys</span></span>
    -   <span data-ttu-id="b33f6-181">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="b33f6-181">vbisurf.ax</span></span>
    -   <span data-ttu-id="b33f6-182">wstcodec.sys</span><span class="sxs-lookup"><span data-stu-id="b33f6-182">wstcodec.sys</span></span>
    -   <span data-ttu-id="b33f6-183">wstdecod.dll</span><span class="sxs-lookup"><span data-stu-id="b33f6-183">wstdecod.dll</span></span>

## <a name="related-topics"></a><span data-ttu-id="b33f6-184">См. также</span><span class="sxs-lookup"><span data-stu-id="b33f6-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b33f6-185">Создание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="b33f6-185">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> </dl>

 

 
