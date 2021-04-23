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
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691286"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="f446b-109">Компиляция IDL-файлов, предоставляемых с помощью пакета SDK</span><span class="sxs-lookup"><span data-stu-id="f446b-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="f446b-110">Пакет Windows Media диспетчер устройств SDK включает как файлы заголовков, так и исходные IDL-файлы для большинства этих файлов заголовков.</span><span class="sxs-lookup"><span data-stu-id="f446b-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="f446b-111">Файлы заголовков находятся в \\ папке Inc \\ в пути установки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="f446b-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="f446b-112">IDL-файлы находятся в \\ \\ папке IDL.</span><span class="sxs-lookup"><span data-stu-id="f446b-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="f446b-113">Предварительно скомпилированные заголовки гораздо проще в использовании, а некоторые файлы IDL объединяются в один предоставленный заголовок.</span><span class="sxs-lookup"><span data-stu-id="f446b-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="f446b-114">Однако если вы решили обработать собственные файлы заголовков из предоставленных IDL-файлов, в этом разделе описывается, какие файлы IDL создают файлы заголовков, а также описывает зависимости каждого IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="f446b-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="f446b-115">**Эквивалентный IDL и предоставленные файлы заголовков**</span><span class="sxs-lookup"><span data-stu-id="f446b-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="f446b-116">**IDL**</span><span class="sxs-lookup"><span data-stu-id="f446b-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="f446b-117">**Эквивалентный указанный заголовок**</span><span class="sxs-lookup"><span data-stu-id="f446b-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="f446b-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f446b-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f446b-119">ВМДМ. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-119">WMDM.idl</span></span><br/> <span data-ttu-id="f446b-120">ВМСП. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-120">WMSP.idl</span></span><br/> <span data-ttu-id="f446b-121">ВМСКП. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-121">WMSCP.idl</span></span><br/> <span data-ttu-id="f446b-122">икомпонентаусентикате. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="f446b-123">Мсвмдм. h</span><span class="sxs-lookup"><span data-stu-id="f446b-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="f446b-124">Все четыре файла IDL включены в этот один указанный заголовок.</span><span class="sxs-lookup"><span data-stu-id="f446b-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="f446b-125">**Вмдм. idl** определяет все интерфейсы приложения, а также необходимые структуры, константы и коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="f446b-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="f446b-126">**Вмсп. idl** определяет все интерфейсы поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="f446b-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="f446b-127">**Вмскп. idl** определяет все интерфейсы, значения GUID и константы, необходимые для защиты поставщиков содержимого.</span><span class="sxs-lookup"><span data-stu-id="f446b-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="f446b-128">**икомпонентаусентикате. idl** определяет интерфейс [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="f446b-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="f446b-129">Вмдмлог. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="f446b-130">Вмдмлог. h</span><span class="sxs-lookup"><span data-stu-id="f446b-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="f446b-131">вмдмлог \_ i. c</span><span class="sxs-lookup"><span data-stu-id="f446b-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="f446b-132">Определяет интерфейсы ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f446b-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="f446b-133">Необходимо использовать оба этих файла заголовков, а не только h-файл, из-за проблемы с файлом IDL.</span><span class="sxs-lookup"><span data-stu-id="f446b-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f446b-134">Вмдрмдевицеапп. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="f446b-135">Вмдрмдевицеапп. h</span><span class="sxs-lookup"><span data-stu-id="f446b-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="f446b-136">Определяет интерфейсы [**ивмдрмдевицеапп**](iwmdrmdeviceapp.md) и [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) , используемые приложениями для обновления управления цифровыми правами на устройствах или счетчиков воспроизведения на устройствах.</span><span class="sxs-lookup"><span data-stu-id="f446b-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="f446b-137">**Зависимости IDL**</span><span class="sxs-lookup"><span data-stu-id="f446b-137">**IDL Dependencies**</span></span>

<span data-ttu-id="f446b-138">Некоторые из предоставленных IDL-файлов имеют зависимости сборки.</span><span class="sxs-lookup"><span data-stu-id="f446b-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="f446b-139">Если вы планируете компилировать IDL-файлы самостоятельно, необходимо обработать эти внешние зависимости в порядке, показанном в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f446b-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f446b-140">**IDL**</span><span class="sxs-lookup"><span data-stu-id="f446b-140">**IDL**</span></span>                    | <span data-ttu-id="f446b-141">**Зависимости**</span><span class="sxs-lookup"><span data-stu-id="f446b-141">**Dependencies**</span></span>                                                                 |
| <span data-ttu-id="f446b-142">икомпонентаусентикате. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="f446b-143">Импортируйте "оаидл. idl";</span><span class="sxs-lookup"><span data-stu-id="f446b-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="f446b-144">\#включить "икомпонентаусентикате. idl"</span><span class="sxs-lookup"><span data-stu-id="f446b-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="f446b-145">ВМДМ. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-145">WMDM.idl</span></span>                   | <span data-ttu-id="f446b-146">Нет внешних зависимостей</span><span class="sxs-lookup"><span data-stu-id="f446b-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="f446b-147">Вмдмлог. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-147">WmdmLog.idl</span></span>                | <span data-ttu-id="f446b-148">Нет внешних зависимостей</span><span class="sxs-lookup"><span data-stu-id="f446b-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="f446b-149">Вмдрмдевицеапп. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="f446b-150">Нет внешних зависимостей</span><span class="sxs-lookup"><span data-stu-id="f446b-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="f446b-151">ВМСКП. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-151">WMSCP.idl</span></span>                  | <span data-ttu-id="f446b-152">\#включить "Вмдрмдевицеапп. idl"</span><span class="sxs-lookup"><span data-stu-id="f446b-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="f446b-153">\#включить "ВМСП. idl"</span><span class="sxs-lookup"><span data-stu-id="f446b-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="f446b-154">ВМСП. idl</span><span class="sxs-lookup"><span data-stu-id="f446b-154">WMSP.idl</span></span>                   | <span data-ttu-id="f446b-155">\#включить "ВМДМ. idl"</span><span class="sxs-lookup"><span data-stu-id="f446b-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="f446b-156">См. также</span><span class="sxs-lookup"><span data-stu-id="f446b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f446b-157">**Задачи, общие для приложений и поставщиков служб**</span><span class="sxs-lookup"><span data-stu-id="f446b-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





