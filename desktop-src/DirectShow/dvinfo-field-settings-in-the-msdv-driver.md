---
description: Параметры полей ДВИНФО в драйвере МСДВ
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Параметры полей ДВИНФО в драйвере МСДВ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806149"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a><span data-ttu-id="03130-103">Параметры полей ДВИНФО в драйвере МСДВ</span><span class="sxs-lookup"><span data-stu-id="03130-103">DVINFO Field Settings in the MSDV Driver</span></span>

<span data-ttu-id="03130-104">В этом разделе описывается, как драйвер МСДВ заполняет структуру [**двинфо**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="03130-104">This section describes how the MSDV driver fills in the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="03130-105">`DVINFO`Структура определяет блок формата для закрепления соединений между мсдв и другими фильтрами.</span><span class="sxs-lookup"><span data-stu-id="03130-105">The `DVINFO` structure defines the format block for pin connections between MSDV and other filters.</span></span> <span data-ttu-id="03130-106">По умолчанию фильтр разделителя DV используется при захвате с устройства DV, а фильтр мультиплексора DV используется при передаче на устройство.</span><span class="sxs-lookup"><span data-stu-id="03130-106">By default, the DV Splitter filter is used when capturing from a DV device, and the DV Mux filter is used when transmitting to the device.</span></span> <span data-ttu-id="03130-107">Однако приложения могут предоставлять собственные настраиваемые фильтры, поэтому полезно понять, как МСДВ заполняет `DVINFO` блок формата.</span><span class="sxs-lookup"><span data-stu-id="03130-107">However, applications may provide their own custom filters, so it is useful to understand how MSDV populates the `DVINFO` format block.</span></span>

<span data-ttu-id="03130-108">`DVINFO`Структура содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="03130-108">The `DVINFO` structure contains the following information:</span></span>

-   <span data-ttu-id="03130-109">Два исходных пакета аудио (ААУКС) для первого и второго звукового блока.</span><span class="sxs-lookup"><span data-stu-id="03130-109">Two audio auxiliary (AAUX) source packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="03130-110">Два пакета управления версиями ААУКС для первого и второго звукового блока.</span><span class="sxs-lookup"><span data-stu-id="03130-110">Two AAUX source control packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="03130-111">Исходный пакет для видео вспомогательного (ВАУКС).</span><span class="sxs-lookup"><span data-stu-id="03130-111">A video auxiliary (VAUX) source pack.</span></span>
-   <span data-ttu-id="03130-112">Пакет управления версиями ВАУКС.</span><span class="sxs-lookup"><span data-stu-id="03130-112">A VAUX source control pack.</span></span>

<span data-ttu-id="03130-113">Каждый кадр в DV-потоке содержит пакеты ААУКС и ВАУКС.</span><span class="sxs-lookup"><span data-stu-id="03130-113">Every frame in a DV stream contains AAUX and VAUX packs.</span></span> <span data-ttu-id="03130-114">Однако `DVINFO` блок формата является статическим и используется только для установления соединения с закреплением.</span><span class="sxs-lookup"><span data-stu-id="03130-114">However, the `DVINFO` format block is static, and is only used to establish the pin connection.</span></span> <span data-ttu-id="03130-115">Когда драйвер МСДВ подключается, он не проверяет ни один из пакетов ААУКС или ВАУКС в потоке.</span><span class="sxs-lookup"><span data-stu-id="03130-115">When the MSDV driver connects, it does not examine any of the AAUX or VAUX packs in the stream.</span></span> <span data-ttu-id="03130-116">Вместо этого используется набор значений по умолчанию, основанный на следующих характеристиках устройства DV:</span><span class="sxs-lookup"><span data-stu-id="03130-116">Instead, it uses a set of default values, based on the following characteristics of the DV device:</span></span>

-   <span data-ttu-id="03130-117">Поддерживает ли устройство формат потребителя (ДВКР) или профессиональный формат (DVCPRO)</span><span class="sxs-lookup"><span data-stu-id="03130-117">Whether the device supports a consumer format (DVCR) or professional format (DVCPRO)</span></span>
-   <span data-ttu-id="03130-118">Тип сигнала</span><span class="sxs-lookup"><span data-stu-id="03130-118">The signal type</span></span>
-   <span data-ttu-id="03130-119">Имеет ли формат NTSC или PAL.</span><span class="sxs-lookup"><span data-stu-id="03130-119">Whether the format is NTSC or PAL.</span></span> <span data-ttu-id="03130-120">(Если устройство не сообщает об этой информации, МСДВ по умолчанию использует параметры NTSC).</span><span class="sxs-lookup"><span data-stu-id="03130-120">(If the device does not report this information, MSDV defaults to the NTSC settings)</span></span>

<span data-ttu-id="03130-121">После начала потоковой передачи ответственность за просмотр фактического содержимого каждого кадра DV осуществляется с помощью фильтров пользовательского режима, таких как разделитель DV.</span><span class="sxs-lookup"><span data-stu-id="03130-121">Once streaming begins, it is the responsibility of the user-mode filters, such as the DV Splitter, to examine the actual contents of each DV frame.</span></span> <span data-ttu-id="03130-122">Так как данные могут изменяться от кадра к кадру, может потребоваться изменение динамического формата.</span><span class="sxs-lookup"><span data-stu-id="03130-122">Because the information can change from frame to frame, the filter may need to perform a dynamic format change.</span></span> <span data-ttu-id="03130-123">Например, при изменении частоты звука фильтр может потребовать повторного согласования типа аудио.</span><span class="sxs-lookup"><span data-stu-id="03130-123">For example, if the audio rate changes, the filter might need to renegotiate the audio type.</span></span>

<span data-ttu-id="03130-124">При записи DV-файла типа 1 `DVINFO` Структура записывается в файл в виде фрагмента формата потока ("стрф").</span><span class="sxs-lookup"><span data-stu-id="03130-124">If you capture a type-1 DV file, the `DVINFO` structure is written into the file as the stream format ('strf') chunk.</span></span> <span data-ttu-id="03130-125">Эти данные берутся непосредственно из блока формата, предоставленного МСДВ.</span><span class="sxs-lookup"><span data-stu-id="03130-125">This data is taken directly from the format block provided by MSDV.</span></span> <span data-ttu-id="03130-126">Как уже отмечалось, реальное содержимое потока может отличаться.</span><span class="sxs-lookup"><span data-stu-id="03130-126">As noted, the actual content of the stream might be different.</span></span> <span data-ttu-id="03130-127">Ответственность за проверку пакетов ААУКС и ВАУКС в каждом кадре несет приложение.</span><span class="sxs-lookup"><span data-stu-id="03130-127">It is the application's responsibility to examine the AAUX and VAUX packs in each frame.</span></span>

<span data-ttu-id="03130-128">В следующих разделах можно найти таблицы со списком всех полей, используемых МСДВ.</span><span class="sxs-lookup"><span data-stu-id="03130-128">In the following topics, you can find tables listing all of the fields used by MSDV.</span></span>

-   [<span data-ttu-id="03130-129">Исходный (AS) пакет ААУКС</span><span class="sxs-lookup"><span data-stu-id="03130-129">AAUX Source (AS) Pack</span></span>](aaux-source--as--pack.md)
-   [<span data-ttu-id="03130-130">Пакет управления версиями ААУКС (ASC)</span><span class="sxs-lookup"><span data-stu-id="03130-130">AAUX Source Control (ASC) Pack</span></span>](aaux-source-control--asc--pack.md)
-   [<span data-ttu-id="03130-131">Пакет ВАУКС (VS)</span><span class="sxs-lookup"><span data-stu-id="03130-131">VAUX Source (VS) Pack</span></span>](vaux-source--vs--pack.md)
-   [<span data-ttu-id="03130-132">Пакет управления версиями ВАУКС (VSC)</span><span class="sxs-lookup"><span data-stu-id="03130-132">VAUX Source Control (VSC) Pack</span></span>](vaux-source-control--vsc--pack.md)

<span data-ttu-id="03130-133">При чтении этих таблиц ознакомьтесь со следующими спецификациями:</span><span class="sxs-lookup"><span data-stu-id="03130-133">When reading these tables, please consult the following specifications:</span></span>

-   <span data-ttu-id="03130-134">IEC 61834</span><span class="sxs-lookup"><span data-stu-id="03130-134">IEC 61834</span></span>
-   <span data-ttu-id="03130-135">SMPTE 314M</span><span class="sxs-lookup"><span data-stu-id="03130-135">SMPTE 314M</span></span>
-   <span data-ttu-id="03130-136">SMPTE 370</span><span class="sxs-lookup"><span data-stu-id="03130-136">SMPTE 370</span></span>

<span data-ttu-id="03130-137">В каждой таблице первый столбец содержит код поля, за которым следует число битов (в круглых скобках).</span><span class="sxs-lookup"><span data-stu-id="03130-137">In each table, the first column gives the field code, followed by the number of bits (in parentheses).</span></span> <span data-ttu-id="03130-138">Оставшиеся столбцы предоставляют значения полей.</span><span class="sxs-lookup"><span data-stu-id="03130-138">The remaining columns give the field values.</span></span> <span data-ttu-id="03130-139">Многие поля ААУКС и ВАУКС не имеют значения для соединения с закреплением. в этом случае МСДВ задает фиктивное значение.</span><span class="sxs-lookup"><span data-stu-id="03130-139">Many of the AAUX and VAUX fields are not relevant for the pin connection, in which case MSDV sets a dummy value.</span></span> <span data-ttu-id="03130-140">Числовое значение всего пакета указано в нижней части каждой таблицы.</span><span class="sxs-lookup"><span data-stu-id="03130-140">The numeric value of the entire pack is listed at the bottom of each table.</span></span>

<span data-ttu-id="03130-141">В примечаниях после каждой таблицы придаются дополнительные сведения о выбранных полях.</span><span class="sxs-lookup"><span data-stu-id="03130-141">The notes after each table give more information about selected fields.</span></span> <span data-ttu-id="03130-142">Полные описания см. в спецификациях.</span><span class="sxs-lookup"><span data-stu-id="03130-142">For complete descriptions, refer to the specifications.</span></span> <span data-ttu-id="03130-143">Кроме того, некоторые поля не имеют одинакового значения в SMPTE 314M/SMPTE 370, как это делается в IEC 61834.</span><span class="sxs-lookup"><span data-stu-id="03130-143">Also, some fields do not have the same meaning in SMPTE 314M/SMPTE 370 as they do in IEC 61834.</span></span>

> [!Note]  
> <span data-ttu-id="03130-144">В настоящее время DirectShow не поддерживает форматы DVCPRO.</span><span class="sxs-lookup"><span data-stu-id="03130-144">Currently, DirectShow does not support DVCPRO formats.</span></span> <span data-ttu-id="03130-145">Значения, перечисленные для форматов DVCPRO, определяются для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="03130-145">The values listed for the DVCPRO formats are defined for future use.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="03130-146">См. также</span><span class="sxs-lookup"><span data-stu-id="03130-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03130-147">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="03130-147">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="03130-148">Данные DV в формате AVI</span><span class="sxs-lookup"><span data-stu-id="03130-148">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[<span data-ttu-id="03130-149">Драйвер МСДВ</span><span class="sxs-lookup"><span data-stu-id="03130-149">MSDV Driver</span></span>](msdv-driver.md)
</dt> </dl>

 

 



