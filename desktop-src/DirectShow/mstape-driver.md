---
description: Драйвер Мстапе
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Драйвер Мстапе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951084f8827f925bba43028c0792736883d5ff0f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909402"
---
# <a name="mstape-driver"></a><span data-ttu-id="9ce39-103">Драйвер Мстапе</span><span class="sxs-lookup"><span data-stu-id="9ce39-103">MSTape Driver</span></span>

<span data-ttu-id="9ce39-104">Этот раздел относится к Windows XP или более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="9ce39-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="9ce39-105">Драйвер Мстапе поддерживает устройства с видеокамеры D-ВХС и MPEG.</span><span class="sxs-lookup"><span data-stu-id="9ce39-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="9ce39-106">Он предоставляется приложениям в качестве фильтра [записи видео WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="9ce39-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="9ce39-107">Его функциональность аналогична функции [мсдв](msdv-driver.md), драйверу видеокамеры.</span><span class="sxs-lookup"><span data-stu-id="9ce39-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="9ce39-108">Он отображается в категориях фильтров "источники видеозаписи (CLSID \_ видеоинпутдевицекатегори)" и "устройства отрисовки WDM Streaming" (преобразование AM \_ кскатегори \_ Render).</span><span class="sxs-lookup"><span data-stu-id="9ce39-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="9ce39-109">Приложение может создать экземпляр фильтра с помощью интерфейса [**икреатедевенум**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="9ce39-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="9ce39-110">Он имеет выходной ПИН-код для захвата и передачи данных с устройства, а также входной ПИН-код для передачи на устройство.</span><span class="sxs-lookup"><span data-stu-id="9ce39-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="9ce39-111">В момент времени может быть подключен только один ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="9ce39-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="9ce39-112">**Типы носителей**</span><span class="sxs-lookup"><span data-stu-id="9ce39-112">**Media Types**</span></span>

<span data-ttu-id="9ce39-113">Входной ПИН-код поддерживает один тип носителя.</span><span class="sxs-lookup"><span data-stu-id="9ce39-113">The input pin supports one media type.</span></span>



| <span data-ttu-id="9ce39-114">Метка</span><span class="sxs-lookup"><span data-stu-id="9ce39-114">Label</span></span> | <span data-ttu-id="9ce39-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce39-115">Value</span></span> |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="9ce39-116">Основной тип</span><span class="sxs-lookup"><span data-stu-id="9ce39-116">Major Type</span></span>   | <span data-ttu-id="9ce39-117">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9ce39-117">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="9ce39-118">Subtype</span><span class="sxs-lookup"><span data-stu-id="9ce39-118">Subtype</span></span>      | <span data-ttu-id="9ce39-119">\_ \_ Шаг транспорта медиасубтипе \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="9ce39-119">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="9ce39-120">Размер выборки</span><span class="sxs-lookup"><span data-stu-id="9ce39-120">Sample Size</span></span>  | <span data-ttu-id="9ce39-121">192 x 256</span><span class="sxs-lookup"><span data-stu-id="9ce39-121">192 x 256</span></span>                                                  |
| <span data-ttu-id="9ce39-122">Блок формата</span><span class="sxs-lookup"><span data-stu-id="9ce39-122">Format Block</span></span> | [<span data-ttu-id="9ce39-123">**\_Шаг транспорта \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="9ce39-123">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="9ce39-124">Выходной закрепление поддерживает два типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9ce39-124">The output pin supports two media types.</span></span>



| <span data-ttu-id="9ce39-125">Метка</span><span class="sxs-lookup"><span data-stu-id="9ce39-125">Label</span></span> | <span data-ttu-id="9ce39-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce39-126">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="9ce39-127">Основной тип</span><span class="sxs-lookup"><span data-stu-id="9ce39-127">Major Type</span></span>   | <span data-ttu-id="9ce39-128">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9ce39-128">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="9ce39-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="9ce39-129">Subtype</span></span>      | <span data-ttu-id="9ce39-130">\_ \_ Шаг транспорта медиасубтипе \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="9ce39-130">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="9ce39-131">Размер выборки</span><span class="sxs-lookup"><span data-stu-id="9ce39-131">Sample Size</span></span>  | <span data-ttu-id="9ce39-132">192 x 256</span><span class="sxs-lookup"><span data-stu-id="9ce39-132">192 x 256</span></span>                              |
| <span data-ttu-id="9ce39-133">Блок формата</span><span class="sxs-lookup"><span data-stu-id="9ce39-133">Format Block</span></span> | <span data-ttu-id="9ce39-134">\_Шаг транспорта \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="9ce39-134">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



| <span data-ttu-id="9ce39-135">Метка</span><span class="sxs-lookup"><span data-stu-id="9ce39-135">Label</span></span> | <span data-ttu-id="9ce39-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce39-136">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="9ce39-137">Основной тип</span><span class="sxs-lookup"><span data-stu-id="9ce39-137">Major Type</span></span>   | <span data-ttu-id="9ce39-138">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9ce39-138">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="9ce39-139">Subtype</span><span class="sxs-lookup"><span data-stu-id="9ce39-139">Subtype</span></span>      | <span data-ttu-id="9ce39-140">\_ \_ Шаг транспорта медиасубтипе \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="9ce39-140">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="9ce39-141">Размер выборки</span><span class="sxs-lookup"><span data-stu-id="9ce39-141">Sample Size</span></span>  | <span data-ttu-id="9ce39-142">188 x 256</span><span class="sxs-lookup"><span data-stu-id="9ce39-142">188 x 256</span></span>                              |
| <span data-ttu-id="9ce39-143">Блок формата</span><span class="sxs-lookup"><span data-stu-id="9ce39-143">Format Block</span></span> | <span data-ttu-id="9ce39-144">**NULL**</span><span class="sxs-lookup"><span data-stu-id="9ce39-144">**NULL**</span></span>                               |



 

<span data-ttu-id="9ce39-145">**Сведения об устройстве**</span><span class="sxs-lookup"><span data-stu-id="9ce39-145">**Device Information**</span></span>

<span data-ttu-id="9ce39-146">Драйвер динамически считывает сведения из ПЗУ конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="9ce39-146">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="9ce39-147">Приложение может получить эти сведения, привязывая моникер устройства к контейнеру свойств и вызвав метод **ипропертибаг:: Read** .</span><span class="sxs-lookup"><span data-stu-id="9ce39-147">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="9ce39-148">Свойство</span><span class="sxs-lookup"><span data-stu-id="9ce39-148">Property</span></span>            | <span data-ttu-id="9ce39-149">Описание</span><span class="sxs-lookup"><span data-stu-id="9ce39-149">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="9ce39-150">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9ce39-150">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="9ce39-151">Уникальный \_ UniqueID</span><span class="sxs-lookup"><span data-stu-id="9ce39-151">UniqueID\_Low</span></span>       | <span data-ttu-id="9ce39-152">Уникальный идентификатор устройства (неограниченный **DWORD**).</span><span class="sxs-lookup"><span data-stu-id="9ce39-152">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="9ce39-153">**Long** (VT \_ i4)</span><span class="sxs-lookup"><span data-stu-id="9ce39-153">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="9ce39-154">Старший уникальный идентификатор \_</span><span class="sxs-lookup"><span data-stu-id="9ce39-154">UniqueID\_High</span></span>      | <span data-ttu-id="9ce39-155">Уникальный идентификатор устройства (High **DWORD**)</span><span class="sxs-lookup"><span data-stu-id="9ce39-155">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="9ce39-156">**long**</span><span class="sxs-lookup"><span data-stu-id="9ce39-156">**long**</span></span>            |
| <span data-ttu-id="9ce39-157">VendorID</span><span class="sxs-lookup"><span data-stu-id="9ce39-157">VendorID</span></span>            | <span data-ttu-id="9ce39-158">Идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="9ce39-158">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="9ce39-159">**long**</span><span class="sxs-lookup"><span data-stu-id="9ce39-159">**long**</span></span>            |
| <span data-ttu-id="9ce39-160">ModelID</span><span class="sxs-lookup"><span data-stu-id="9ce39-160">ModelID</span></span>             | <span data-ttu-id="9ce39-161">Идентификатор модели.</span><span class="sxs-lookup"><span data-stu-id="9ce39-161">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="9ce39-162">**long**</span><span class="sxs-lookup"><span data-stu-id="9ce39-162">**long**</span></span>            |
| <span data-ttu-id="9ce39-163">вендортекст</span><span class="sxs-lookup"><span data-stu-id="9ce39-163">VendorText</span></span>          | <span data-ttu-id="9ce39-164">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="9ce39-164">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="9ce39-165">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="9ce39-165">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="9ce39-166">моделтекст</span><span class="sxs-lookup"><span data-stu-id="9ce39-166">ModelText</span></span>           | <span data-ttu-id="9ce39-167">Имя модели устройства.</span><span class="sxs-lookup"><span data-stu-id="9ce39-167">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="9ce39-168">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="9ce39-168">**BSTR**</span></span>            |
| <span data-ttu-id="9ce39-169">унитмоделтекст</span><span class="sxs-lookup"><span data-stu-id="9ce39-169">UnitModelText</span></span>       | <span data-ttu-id="9ce39-170">Имя модели единицы измерения; может совпадать с Моделтекст.</span><span class="sxs-lookup"><span data-stu-id="9ce39-170">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="9ce39-171">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="9ce39-171">**BSTR**</span></span>            |
| <span data-ttu-id="9ce39-172">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="9ce39-172">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="9ce39-173">полезные данные Опкр (Управление подключаемым модулем вывода).</span><span class="sxs-lookup"><span data-stu-id="9ce39-173">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="9ce39-174">Пример: 146 куадлетс.</span><span class="sxs-lookup"><span data-stu-id="9ce39-174">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="9ce39-175">**long**</span><span class="sxs-lookup"><span data-stu-id="9ce39-175">**long**</span></span>            |
| <span data-ttu-id="9ce39-176">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="9ce39-176">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="9ce39-177">скорость передачи данных Опкр.</span><span class="sxs-lookup"><span data-stu-id="9ce39-177">oPCR data rate.</span></span> <span data-ttu-id="9ce39-178">Примеры: 0 (S100), 1 (S200) или 2 (S400).</span><span class="sxs-lookup"><span data-stu-id="9ce39-178">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="9ce39-179">**long**</span><span class="sxs-lookup"><span data-stu-id="9ce39-179">**long**</span></span>            |
| <span data-ttu-id="9ce39-180">девицеклассгуид</span><span class="sxs-lookup"><span data-stu-id="9ce39-180">DeviceClassGUID</span></span>     | <span data-ttu-id="9ce39-181">Идентификатор GUID, определяющий драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="9ce39-181">GUID that identifies the device driver.</span></span> <span data-ttu-id="9ce39-182">Для Мстапе это значение равно `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="9ce39-182">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="9ce39-183">Этот идентификатор GUID определен как Мстапедевицегуид в файле заголовка Кспртдефс. h.</span><span class="sxs-lookup"><span data-stu-id="9ce39-183">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="9ce39-184">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="9ce39-184">**BSTR**</span></span>            |
| <span data-ttu-id="9ce39-185">Описание</span><span class="sxs-lookup"><span data-stu-id="9ce39-185">Description</span></span>         | <span data-ttu-id="9ce39-186">Описание устройства, взятое из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="9ce39-186">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="9ce39-187">Эта строка обычно содержит название торговой марки устройства.</span><span class="sxs-lookup"><span data-stu-id="9ce39-187">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="9ce39-188">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="9ce39-188">**BSTR**</span></span>            |



 

<span data-ttu-id="9ce39-189">ИДЕНТИФИКАТОР устройства — это 64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="9ce39-189">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="9ce39-190">Нижний **DWORD** хранится в \_ свойстве UniqueID  Low, а High — в \_ свойстве UniqueID High.</span><span class="sxs-lookup"><span data-stu-id="9ce39-190">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="9ce39-191">Дополнительные сведения об моникерах устройств см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="9ce39-191">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ce39-192">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9ce39-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ce39-193">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="9ce39-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="9ce39-194">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="9ce39-194">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



