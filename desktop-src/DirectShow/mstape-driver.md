---
description: Драйвер Мстапе
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Драйвер Мстапе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894106"
---
# <a name="mstape-driver"></a><span data-ttu-id="7eee6-103">Драйвер Мстапе</span><span class="sxs-lookup"><span data-stu-id="7eee6-103">MSTape Driver</span></span>

<span data-ttu-id="7eee6-104">Этот раздел относится к Windows XP или более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="7eee6-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="7eee6-105">Драйвер Мстапе поддерживает устройства с видеокамеры D-ВХС и MPEG.</span><span class="sxs-lookup"><span data-stu-id="7eee6-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="7eee6-106">Он предоставляется приложениям в качестве фильтра [записи видео WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7eee6-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="7eee6-107">Его функциональность аналогична функции [мсдв](msdv-driver.md), драйверу видеокамеры.</span><span class="sxs-lookup"><span data-stu-id="7eee6-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="7eee6-108">Он отображается в категориях фильтров "источники видеозаписи (CLSID \_ видеоинпутдевицекатегори)" и "устройства отрисовки WDM Streaming" (преобразование AM \_ кскатегори \_ Render).</span><span class="sxs-lookup"><span data-stu-id="7eee6-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="7eee6-109">Приложение может создать экземпляр фильтра с помощью интерфейса [**икреатедевенум**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="7eee6-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="7eee6-110">Он имеет выходной ПИН-код для захвата и передачи данных с устройства, а также входной ПИН-код для передачи на устройство.</span><span class="sxs-lookup"><span data-stu-id="7eee6-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="7eee6-111">В момент времени может быть подключен только один ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="7eee6-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="7eee6-112">**Типы носителей**</span><span class="sxs-lookup"><span data-stu-id="7eee6-112">**Media Types**</span></span>

<span data-ttu-id="7eee6-113">Входной ПИН-код поддерживает один тип носителя.</span><span class="sxs-lookup"><span data-stu-id="7eee6-113">The input pin supports one media type.</span></span>



|              |                                                            |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="7eee6-114">Основной тип</span><span class="sxs-lookup"><span data-stu-id="7eee6-114">Major Type</span></span>   | <span data-ttu-id="7eee6-115">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7eee6-115">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="7eee6-116">Subtype</span><span class="sxs-lookup"><span data-stu-id="7eee6-116">Subtype</span></span>      | <span data-ttu-id="7eee6-117">\_ \_ Шаг транспорта медиасубтипе \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="7eee6-117">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="7eee6-118">Размер выборки</span><span class="sxs-lookup"><span data-stu-id="7eee6-118">Sample Size</span></span>  | <span data-ttu-id="7eee6-119">192 x 256</span><span class="sxs-lookup"><span data-stu-id="7eee6-119">192 x 256</span></span>                                                  |
| <span data-ttu-id="7eee6-120">Блок формата</span><span class="sxs-lookup"><span data-stu-id="7eee6-120">Format Block</span></span> | [<span data-ttu-id="7eee6-121">**\_Шаг транспорта \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="7eee6-121">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="7eee6-122">Выходной закрепление поддерживает два типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7eee6-122">The output pin supports two media types.</span></span>



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="7eee6-123">Основной тип</span><span class="sxs-lookup"><span data-stu-id="7eee6-123">Major Type</span></span>   | <span data-ttu-id="7eee6-124">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7eee6-124">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="7eee6-125">Subtype</span><span class="sxs-lookup"><span data-stu-id="7eee6-125">Subtype</span></span>      | <span data-ttu-id="7eee6-126">\_ \_ Шаг транспорта медиасубтипе \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="7eee6-126">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="7eee6-127">Размер выборки</span><span class="sxs-lookup"><span data-stu-id="7eee6-127">Sample Size</span></span>  | <span data-ttu-id="7eee6-128">192 x 256</span><span class="sxs-lookup"><span data-stu-id="7eee6-128">192 x 256</span></span>                              |
| <span data-ttu-id="7eee6-129">Блок формата</span><span class="sxs-lookup"><span data-stu-id="7eee6-129">Format Block</span></span> | <span data-ttu-id="7eee6-130">\_Шаг транспорта \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="7eee6-130">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="7eee6-131">Основной тип</span><span class="sxs-lookup"><span data-stu-id="7eee6-131">Major Type</span></span>   | <span data-ttu-id="7eee6-132">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7eee6-132">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="7eee6-133">Subtype</span><span class="sxs-lookup"><span data-stu-id="7eee6-133">Subtype</span></span>      | <span data-ttu-id="7eee6-134">\_ \_ Шаг транспорта медиасубтипе \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="7eee6-134">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="7eee6-135">Размер выборки</span><span class="sxs-lookup"><span data-stu-id="7eee6-135">Sample Size</span></span>  | <span data-ttu-id="7eee6-136">188 x 256</span><span class="sxs-lookup"><span data-stu-id="7eee6-136">188 x 256</span></span>                              |
| <span data-ttu-id="7eee6-137">Блок формата</span><span class="sxs-lookup"><span data-stu-id="7eee6-137">Format Block</span></span> | <span data-ttu-id="7eee6-138">**NULL**</span><span class="sxs-lookup"><span data-stu-id="7eee6-138">**NULL**</span></span>                               |



 

<span data-ttu-id="7eee6-139">**Сведения об устройстве**</span><span class="sxs-lookup"><span data-stu-id="7eee6-139">**Device Information**</span></span>

<span data-ttu-id="7eee6-140">Драйвер динамически считывает сведения из ПЗУ конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="7eee6-140">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="7eee6-141">Приложение может получить эти сведения, привязывая моникер устройства к контейнеру свойств и вызвав метод **ипропертибаг:: Read** .</span><span class="sxs-lookup"><span data-stu-id="7eee6-141">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="7eee6-142">Свойство</span><span class="sxs-lookup"><span data-stu-id="7eee6-142">Property</span></span>            | <span data-ttu-id="7eee6-143">Описание</span><span class="sxs-lookup"><span data-stu-id="7eee6-143">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="7eee6-144">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7eee6-144">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7eee6-145">Уникальный \_ UniqueID</span><span class="sxs-lookup"><span data-stu-id="7eee6-145">UniqueID\_Low</span></span>       | <span data-ttu-id="7eee6-146">Уникальный идентификатор устройства (неограниченный **DWORD**).</span><span class="sxs-lookup"><span data-stu-id="7eee6-146">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="7eee6-147">**Long** (VT \_ i4)</span><span class="sxs-lookup"><span data-stu-id="7eee6-147">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="7eee6-148">Старший уникальный идентификатор \_</span><span class="sxs-lookup"><span data-stu-id="7eee6-148">UniqueID\_High</span></span>      | <span data-ttu-id="7eee6-149">Уникальный идентификатор устройства (High **DWORD**)</span><span class="sxs-lookup"><span data-stu-id="7eee6-149">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="7eee6-150">**long**</span><span class="sxs-lookup"><span data-stu-id="7eee6-150">**long**</span></span>            |
| <span data-ttu-id="7eee6-151">VendorID</span><span class="sxs-lookup"><span data-stu-id="7eee6-151">VendorID</span></span>            | <span data-ttu-id="7eee6-152">Идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="7eee6-152">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="7eee6-153">**long**</span><span class="sxs-lookup"><span data-stu-id="7eee6-153">**long**</span></span>            |
| <span data-ttu-id="7eee6-154">ModelID</span><span class="sxs-lookup"><span data-stu-id="7eee6-154">ModelID</span></span>             | <span data-ttu-id="7eee6-155">Идентификатор модели.</span><span class="sxs-lookup"><span data-stu-id="7eee6-155">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="7eee6-156">**long**</span><span class="sxs-lookup"><span data-stu-id="7eee6-156">**long**</span></span>            |
| <span data-ttu-id="7eee6-157">вендортекст</span><span class="sxs-lookup"><span data-stu-id="7eee6-157">VendorText</span></span>          | <span data-ttu-id="7eee6-158">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="7eee6-158">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="7eee6-159">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="7eee6-159">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="7eee6-160">моделтекст</span><span class="sxs-lookup"><span data-stu-id="7eee6-160">ModelText</span></span>           | <span data-ttu-id="7eee6-161">Имя модели устройства.</span><span class="sxs-lookup"><span data-stu-id="7eee6-161">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="7eee6-162">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="7eee6-162">**BSTR**</span></span>            |
| <span data-ttu-id="7eee6-163">унитмоделтекст</span><span class="sxs-lookup"><span data-stu-id="7eee6-163">UnitModelText</span></span>       | <span data-ttu-id="7eee6-164">Имя модели единицы измерения; может совпадать с Моделтекст.</span><span class="sxs-lookup"><span data-stu-id="7eee6-164">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="7eee6-165">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="7eee6-165">**BSTR**</span></span>            |
| <span data-ttu-id="7eee6-166">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="7eee6-166">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="7eee6-167">полезные данные Опкр (Управление подключаемым модулем вывода).</span><span class="sxs-lookup"><span data-stu-id="7eee6-167">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="7eee6-168">Пример: 146 куадлетс.</span><span class="sxs-lookup"><span data-stu-id="7eee6-168">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="7eee6-169">**long**</span><span class="sxs-lookup"><span data-stu-id="7eee6-169">**long**</span></span>            |
| <span data-ttu-id="7eee6-170">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="7eee6-170">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="7eee6-171">скорость передачи данных Опкр.</span><span class="sxs-lookup"><span data-stu-id="7eee6-171">oPCR data rate.</span></span> <span data-ttu-id="7eee6-172">Примеры: 0 (S100), 1 (S200) или 2 (S400).</span><span class="sxs-lookup"><span data-stu-id="7eee6-172">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="7eee6-173">**long**</span><span class="sxs-lookup"><span data-stu-id="7eee6-173">**long**</span></span>            |
| <span data-ttu-id="7eee6-174">девицеклассгуид</span><span class="sxs-lookup"><span data-stu-id="7eee6-174">DeviceClassGUID</span></span>     | <span data-ttu-id="7eee6-175">Идентификатор GUID, определяющий драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="7eee6-175">GUID that identifies the device driver.</span></span> <span data-ttu-id="7eee6-176">Для Мстапе это значение равно `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="7eee6-176">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="7eee6-177">Этот идентификатор GUID определен как Мстапедевицегуид в файле заголовка Кспртдефс. h.</span><span class="sxs-lookup"><span data-stu-id="7eee6-177">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="7eee6-178">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="7eee6-178">**BSTR**</span></span>            |
| <span data-ttu-id="7eee6-179">Описание</span><span class="sxs-lookup"><span data-stu-id="7eee6-179">Description</span></span>         | <span data-ttu-id="7eee6-180">Описание устройства, взятое из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="7eee6-180">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="7eee6-181">Эта строка обычно содержит название торговой марки устройства.</span><span class="sxs-lookup"><span data-stu-id="7eee6-181">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="7eee6-182">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="7eee6-182">**BSTR**</span></span>            |



 

<span data-ttu-id="7eee6-183">ИДЕНТИФИКАТОР устройства — это 64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="7eee6-183">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="7eee6-184">Нижний **DWORD** хранится в \_ свойстве UniqueID  Low, а High — в \_ свойстве UniqueID High.</span><span class="sxs-lookup"><span data-stu-id="7eee6-184">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="7eee6-185">Дополнительные сведения об моникерах устройств см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="7eee6-185">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eee6-186">См. также</span><span class="sxs-lookup"><span data-stu-id="7eee6-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eee6-187">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="7eee6-187">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="7eee6-188">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="7eee6-188">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



