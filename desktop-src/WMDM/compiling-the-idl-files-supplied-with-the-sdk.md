---
title: Компиляция IDL-файлов, предоставляемых с помощью пакета SDK
description: Компиляция IDL-файлов, предоставляемых с помощью пакета SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Диспетчер устройств Windows Media, IDL-файлы
- Диспетчер устройств, IDL-файлы
- Классические приложения, IDL-файлы
- поставщики услуг, IDL-файлы
- инструкции по программированию, IDL-файлы
- IDL-файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444015"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="366f7-109">Компиляция IDL-файлов, предоставляемых с помощью пакета SDK</span><span class="sxs-lookup"><span data-stu-id="366f7-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="366f7-110">Пакет Windows Media диспетчер устройств SDK включает как файлы заголовков, так и исходные IDL-файлы для большинства этих файлов заголовков.</span><span class="sxs-lookup"><span data-stu-id="366f7-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="366f7-111">Файлы заголовков находятся в \\ папке Inc \\ в пути установки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="366f7-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="366f7-112">IDL-файлы находятся в \\ \\ папке IDL.</span><span class="sxs-lookup"><span data-stu-id="366f7-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="366f7-113">Предварительно скомпилированные заголовки гораздо проще в использовании, а некоторые файлы IDL объединяются в один предоставленный заголовок.</span><span class="sxs-lookup"><span data-stu-id="366f7-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="366f7-114">Однако если вы решили обработать собственные файлы заголовков из предоставленных IDL-файлов, в этом разделе описывается, какие файлы IDL создают файлы заголовков, а также описывает зависимости каждого IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="366f7-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="366f7-115">**Эквивалентный IDL и предоставленные файлы заголовков**</span><span class="sxs-lookup"><span data-stu-id="366f7-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="366f7-116">**IDL**</span><span class="sxs-lookup"><span data-stu-id="366f7-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="366f7-117">**Эквивалентный указанный заголовок**</span><span class="sxs-lookup"><span data-stu-id="366f7-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="366f7-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="366f7-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="366f7-119">ВМДМ. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-119">WMDM.idl</span></span><br/> <span data-ttu-id="366f7-120">ВМСП. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-120">WMSP.idl</span></span><br/> <span data-ttu-id="366f7-121">ВМСКП. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-121">WMSCP.idl</span></span><br/> <span data-ttu-id="366f7-122">икомпонентаусентикате. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="366f7-123">Мсвмдм. h</span><span class="sxs-lookup"><span data-stu-id="366f7-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="366f7-124">Все четыре файла IDL включены в этот один указанный заголовок.</span><span class="sxs-lookup"><span data-stu-id="366f7-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="366f7-125">**Вмдм. idl** определяет все интерфейсы приложения, а также необходимые структуры, константы и коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="366f7-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="366f7-126">**Вмсп. idl** определяет все интерфейсы поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="366f7-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="366f7-127">**Вмскп. idl** определяет все интерфейсы, значения GUID и константы, необходимые для защиты поставщиков содержимого.</span><span class="sxs-lookup"><span data-stu-id="366f7-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="366f7-128">**икомпонентаусентикате. idl** определяет интерфейс [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="366f7-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="366f7-129">Вмдмлог. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="366f7-130">Вмдмлог. h</span><span class="sxs-lookup"><span data-stu-id="366f7-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="366f7-131">вмдмлог \_ i. c</span><span class="sxs-lookup"><span data-stu-id="366f7-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="366f7-132">Определяет интерфейсы ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="366f7-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="366f7-133">Необходимо использовать оба этих файла заголовков, а не только h-файл, из-за проблемы с файлом IDL.</span><span class="sxs-lookup"><span data-stu-id="366f7-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="366f7-134">Вмдрмдевицеапп. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="366f7-135">Вмдрмдевицеапп. h</span><span class="sxs-lookup"><span data-stu-id="366f7-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="366f7-136">Определяет интерфейсы [**ивмдрмдевицеапп**](iwmdrmdeviceapp.md) и [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) , используемые приложениями для обновления управления цифровыми правами на устройствах или счетчиков воспроизведения на устройствах.</span><span class="sxs-lookup"><span data-stu-id="366f7-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="366f7-137">**Зависимости IDL**</span><span class="sxs-lookup"><span data-stu-id="366f7-137">**IDL Dependencies**</span></span>

<span data-ttu-id="366f7-138">Некоторые из предоставленных IDL-файлов имеют зависимости сборки.</span><span class="sxs-lookup"><span data-stu-id="366f7-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="366f7-139">Если вы планируете компилировать IDL-файлы самостоятельно, необходимо обработать эти внешние зависимости в порядке, показанном в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="366f7-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|   <span data-ttu-id="366f7-140">IDL</span><span class="sxs-lookup"><span data-stu-id="366f7-140">IDL</span></span>                      |   <span data-ttu-id="366f7-141">Зависимости</span><span class="sxs-lookup"><span data-stu-id="366f7-141">Dependencies</span></span>                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="366f7-142">икомпонентаусентикате. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="366f7-143">Импортируйте "оаидл. idl";</span><span class="sxs-lookup"><span data-stu-id="366f7-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="366f7-144">\#включить "икомпонентаусентикате. idl"</span><span class="sxs-lookup"><span data-stu-id="366f7-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="366f7-145">ВМДМ. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-145">WMDM.idl</span></span>                   | <span data-ttu-id="366f7-146">Отсутствие внешних зависимостей</span><span class="sxs-lookup"><span data-stu-id="366f7-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="366f7-147">Вмдмлог. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-147">WmdmLog.idl</span></span>                | <span data-ttu-id="366f7-148">Отсутствие внешних зависимостей</span><span class="sxs-lookup"><span data-stu-id="366f7-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="366f7-149">Вмдрмдевицеапп. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="366f7-150">Отсутствие внешних зависимостей</span><span class="sxs-lookup"><span data-stu-id="366f7-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="366f7-151">ВМСКП. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-151">WMSCP.idl</span></span>                  | <span data-ttu-id="366f7-152">\#включить "Вмдрмдевицеапп. idl"</span><span class="sxs-lookup"><span data-stu-id="366f7-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="366f7-153">\#включить "ВМСП. idl"</span><span class="sxs-lookup"><span data-stu-id="366f7-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="366f7-154">ВМСП. idl</span><span class="sxs-lookup"><span data-stu-id="366f7-154">WMSP.idl</span></span>                   | <span data-ttu-id="366f7-155">\#включить "ВМДМ. idl"</span><span class="sxs-lookup"><span data-stu-id="366f7-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="366f7-156">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="366f7-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="366f7-157">**Задачи, общие для приложений и поставщиков служб**</span><span class="sxs-lookup"><span data-stu-id="366f7-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





