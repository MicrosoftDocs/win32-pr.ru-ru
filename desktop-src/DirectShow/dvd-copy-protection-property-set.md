---
description: Набор свойств защита от копирования DVD-дисков обеспечивает проверку подлинности данных для защиты от копирования с помощью аппаратных или программных дешифрования. Это свойство используется для предотвращения несанкционированного копирования с предварительно записанного DVD-видео.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Набор свойств защиты от копирования DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909482"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="c0449-104">Набор свойств защиты копирования DVD-дисков</span><span class="sxs-lookup"><span data-stu-id="c0449-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="c0449-105">Набор свойств защита от копирования DVD-дисков обеспечивает проверку подлинности данных для защиты от копирования с помощью аппаратных или программных дешифрования.</span><span class="sxs-lookup"><span data-stu-id="c0449-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="c0449-106">Это свойство используется для предотвращения несанкционированного копирования с предварительно записанного DVD-видео.</span><span class="sxs-lookup"><span data-stu-id="c0449-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="c0449-107">Корпорация Майкрософт предоставляет программное обеспечение, которое упрощает процесс проверки подлинности, необходимый для схемы шифрования, тем самым позволяя дисководу DVD-дисков выполнять проверку подлинности и перенос ключей с помощью дешифрования DVD.</span><span class="sxs-lookup"><span data-stu-id="c0449-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="c0449-108">Корпорация Майкрософт не имеет текущих планов по отправке DVD-дешифрования и, вместо этого, предоставляет код операционной системы, который будет служить агентом для проверки подлинности программных и аппаратных дешифрования.</span><span class="sxs-lookup"><span data-stu-id="c0449-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="c0449-109">Навигатор DVD инициирует и контролирует процесс обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="c0449-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="c0449-110">Минидривер DVD должен только реализовать следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0449-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="c0449-111">Остальные компоненты обработают остальные.</span><span class="sxs-lookup"><span data-stu-id="c0449-111">Other components handle the rest.</span></span>

<span data-ttu-id="c0449-112">Каждый входной поток DVD-диска получит свойства защиты копирования.</span><span class="sxs-lookup"><span data-stu-id="c0449-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="c0449-113">Это справедливо даже в том случае, если одно и то же оборудование управляет всеми потоками DVD.</span><span class="sxs-lookup"><span data-stu-id="c0449-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="c0449-114">Следующая информация представляет необходимые константы и типы данных, используемые для этого свойства в вызовах методов [**икспропертисет**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="c0449-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="c0449-115">Он предоставляет значения для параметров **GUID** (*ГУИДПРОПСЕТ*), идентификатора свойства (*dwPropID*) и типа данных свойства (*ппропдата*).</span><span class="sxs-lookup"><span data-stu-id="c0449-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="c0449-116">Метка</span><span class="sxs-lookup"><span data-stu-id="c0449-116">Label</span></span> | <span data-ttu-id="c0449-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c0449-117">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="c0449-118">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="c0449-118">Property Set GUID</span></span> | <span data-ttu-id="c0449-119">\_Кспропсетид \_ копипрот</span><span class="sxs-lookup"><span data-stu-id="c0449-119">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0449-120">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="c0449-120">Property ID</span></span></th>
<th><span data-ttu-id="c0449-121">Описание</span><span class="sxs-lookup"><span data-stu-id="c0449-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0449-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c0449-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="c0449-123">Запрашивает, является ли вывод видео стандартным — определением аналогового компонента.</span><span class="sxs-lookup"><span data-stu-id="c0449-123">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0449-124">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="c0449-124">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="c0449-125">Это свойство только для установки.</span><span class="sxs-lookup"><span data-stu-id="c0449-125">This is a set-only property.</span></span> <span data-ttu-id="c0449-126">Это свойство устанавливает аналоговый уровень защиты копирования для кодировщика NTSC на выходном конце принимающего ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c0449-126">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="c0449-127">Использует <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0449-127">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0449-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="c0449-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="c0449-129">В этом свойстве поддерживаются обе операции Get и Set.</span><span class="sxs-lookup"><span data-stu-id="c0449-129">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="c0449-130">Операция Get запрашивает у декодера ввод ключа вызова шины.</span><span class="sxs-lookup"><span data-stu-id="c0449-130">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="c0449-131">Операция Set предоставляет декодеру ключ вызова шины с DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="c0449-131">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="c0449-132">Данные, передаваемые в этом свойстве, будут представлять собой структуру типа <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0449-132">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0449-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="c0449-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="c0449-134">Это свойство только для получения.</span><span class="sxs-lookup"><span data-stu-id="c0449-134">This is a get-only property.</span></span> <span data-ttu-id="c0449-135">Это свойство запрашивает передачу ключа шины 2 декодера на DVD-дисковод.</span><span class="sxs-lookup"><span data-stu-id="c0449-135">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="c0449-136">Передаваемые данные будут представлять собой структуру типа <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0449-136">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0449-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="c0449-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="c0449-138">Свойство только для установки.</span><span class="sxs-lookup"><span data-stu-id="c0449-138">Set-only property.</span></span> <span data-ttu-id="c0449-139">Это обеспечивает ключ диска.</span><span class="sxs-lookup"><span data-stu-id="c0449-139">This provides disc key.</span></span> <span data-ttu-id="c0449-140">Ключ представляет собой структуру типа <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0449-140">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0449-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="c0449-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="c0449-142">Это свойство только для установки.</span><span class="sxs-lookup"><span data-stu-id="c0449-142">This is a set-only property.</span></span> <span data-ttu-id="c0449-143">Это свойство предоставляет декодеру канал 1 шины DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="c0449-143">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="c0449-144">Передаваемые данные будут представлять собой структуру типа <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0449-144">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0449-145">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="c0449-145">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="c0449-146">Код региона запрашивает определение региона, которое может играть декодер, в соответствии с определением в консорциуме DVD.</span><span class="sxs-lookup"><span data-stu-id="c0449-146">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="c0449-147">Этот регион определен как структура <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c0449-147">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0449-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="c0449-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="c0449-149">В этом свойстве поддерживаются оба варианта: Get и Set.</span><span class="sxs-lookup"><span data-stu-id="c0449-149">Both get and set are supported on this property.</span></span> <span data-ttu-id="c0449-150">Сначала вызывается метод Get, чтобы определить, требуется ли проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="c0449-150">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="c0449-151">Свойства набора указывают на фазу согласования защиты копирования, которую вводит фильтр.</span><span class="sxs-lookup"><span data-stu-id="c0449-151">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="c0449-152">Передаваемые данные будут представлять собой структуру типа <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0449-152">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0449-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="c0449-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="c0449-154">Если это свойство имеет <strong>значение true</strong>, Навигатор DVD не отправляет образцы <strong>AM_UseNewCSSKey</strong> перед согласованием ключа диска.</span><span class="sxs-lookup"><span data-stu-id="c0449-154">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="c0449-155">См. <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0449-155">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="c0449-156">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c0449-156">Read-only.</span></span> <span data-ttu-id="c0449-157">Данные свойства являются <strong>логическим</strong> значением.</span><span class="sxs-lookup"><span data-stu-id="c0449-157">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0449-158">Применяется к Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0449-158">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0449-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="c0449-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="c0449-160">Это свойство только для установки.</span><span class="sxs-lookup"><span data-stu-id="c0449-160">This is a set-only property.</span></span> <span data-ttu-id="c0449-161">Он предоставляет ключ заголовка из текущего содержимого.</span><span class="sxs-lookup"><span data-stu-id="c0449-161">This provides title key from current content.</span></span> <span data-ttu-id="c0449-162">Ключ представляет собой структуру типа <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0449-162">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c0449-163">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="c0449-163">Requirements</span></span>



| <span data-ttu-id="c0449-164">Требование</span><span class="sxs-lookup"><span data-stu-id="c0449-164">Requirement</span></span> | <span data-ttu-id="c0449-165">Значение</span><span class="sxs-lookup"><span data-stu-id="c0449-165">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0449-166">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c0449-166">Header</span></span><br/> | <dl> <span data-ttu-id="c0449-167"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0449-167"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0449-168">См. также</span><span class="sxs-lookup"><span data-stu-id="c0449-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0449-169">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="c0449-169">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




