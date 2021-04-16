---
description: Набор свойств защита от копирования DVD-дисков обеспечивает проверку подлинности данных для защиты от копирования с помощью аппаратных или программных дешифрования. Это свойство используется для предотвращения несанкционированного копирования с предварительно записанного DVD-видео.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Набор свойств защиты от копирования DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679738"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="4acfc-104">Набор свойств защиты копирования DVD-дисков</span><span class="sxs-lookup"><span data-stu-id="4acfc-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="4acfc-105">Набор свойств защита от копирования DVD-дисков обеспечивает проверку подлинности данных для защиты от копирования с помощью аппаратных или программных дешифрования.</span><span class="sxs-lookup"><span data-stu-id="4acfc-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="4acfc-106">Это свойство используется для предотвращения несанкционированного копирования с предварительно записанного DVD-видео.</span><span class="sxs-lookup"><span data-stu-id="4acfc-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="4acfc-107">Корпорация Майкрософт предоставляет программное обеспечение, которое упрощает процесс проверки подлинности, необходимый для схемы шифрования, тем самым позволяя дисководу DVD-дисков выполнять проверку подлинности и перенос ключей с помощью дешифрования DVD.</span><span class="sxs-lookup"><span data-stu-id="4acfc-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="4acfc-108">Корпорация Майкрософт не имеет текущих планов по отправке DVD-дешифрования и, вместо этого, предоставляет код операционной системы, который будет служить агентом для проверки подлинности программных и аппаратных дешифрования.</span><span class="sxs-lookup"><span data-stu-id="4acfc-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="4acfc-109">Навигатор DVD инициирует и контролирует процесс обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="4acfc-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="4acfc-110">Минидривер DVD должен только реализовать следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4acfc-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="4acfc-111">Остальные компоненты обработают остальные.</span><span class="sxs-lookup"><span data-stu-id="4acfc-111">Other components handle the rest.</span></span>

<span data-ttu-id="4acfc-112">Каждый входной поток DVD-диска получит свойства защиты копирования.</span><span class="sxs-lookup"><span data-stu-id="4acfc-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="4acfc-113">Это справедливо даже в том случае, если одно и то же оборудование управляет всеми потоками DVD.</span><span class="sxs-lookup"><span data-stu-id="4acfc-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="4acfc-114">Следующая информация представляет необходимые константы и типы данных, используемые для этого свойства в вызовах методов [**икспропертисет**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="4acfc-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="4acfc-115">Он предоставляет значения для параметров **GUID** (*ГУИДПРОПСЕТ*), идентификатора свойства (*dwPropID*) и типа данных свойства (*ппропдата*).</span><span class="sxs-lookup"><span data-stu-id="4acfc-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="4acfc-116">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="4acfc-116">Property Set GUID</span></span> | <span data-ttu-id="4acfc-117">\_Кспропсетид \_ копипрот</span><span class="sxs-lookup"><span data-stu-id="4acfc-117">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4acfc-118">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="4acfc-118">Property ID</span></span></th>
<th><span data-ttu-id="4acfc-119">Описание</span><span class="sxs-lookup"><span data-stu-id="4acfc-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4acfc-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4acfc-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="4acfc-121">Запрашивает, является ли вывод видео стандартным — определением аналогового компонента.</span><span class="sxs-lookup"><span data-stu-id="4acfc-121">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4acfc-122">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="4acfc-122">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="4acfc-123">Это свойство только для установки.</span><span class="sxs-lookup"><span data-stu-id="4acfc-123">This is a set-only property.</span></span> <span data-ttu-id="4acfc-124">Это свойство устанавливает аналоговый уровень защиты копирования для кодировщика NTSC на выходном конце принимающего ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="4acfc-124">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="4acfc-125">Использует <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4acfc-125">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4acfc-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="4acfc-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="4acfc-127">В этом свойстве поддерживаются обе операции Get и Set.</span><span class="sxs-lookup"><span data-stu-id="4acfc-127">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="4acfc-128">Операция Get запрашивает у декодера ввод ключа вызова шины.</span><span class="sxs-lookup"><span data-stu-id="4acfc-128">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="4acfc-129">Операция Set предоставляет декодеру ключ вызова шины с DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="4acfc-129">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="4acfc-130">Данные, передаваемые в этом свойстве, будут представлять собой структуру типа <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4acfc-130">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4acfc-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="4acfc-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="4acfc-132">Это свойство только для получения.</span><span class="sxs-lookup"><span data-stu-id="4acfc-132">This is a get-only property.</span></span> <span data-ttu-id="4acfc-133">Это свойство запрашивает передачу ключа шины 2 декодера на DVD-дисковод.</span><span class="sxs-lookup"><span data-stu-id="4acfc-133">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="4acfc-134">Передаваемые данные будут представлять собой структуру типа <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4acfc-134">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4acfc-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="4acfc-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="4acfc-136">Свойство только для установки.</span><span class="sxs-lookup"><span data-stu-id="4acfc-136">Set-only property.</span></span> <span data-ttu-id="4acfc-137">Это обеспечивает ключ диска.</span><span class="sxs-lookup"><span data-stu-id="4acfc-137">This provides disc key.</span></span> <span data-ttu-id="4acfc-138">Ключ представляет собой структуру типа <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4acfc-138">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4acfc-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="4acfc-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="4acfc-140">Это свойство только для установки.</span><span class="sxs-lookup"><span data-stu-id="4acfc-140">This is a set-only property.</span></span> <span data-ttu-id="4acfc-141">Это свойство предоставляет декодеру канал 1 шины DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="4acfc-141">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="4acfc-142">Передаваемые данные будут представлять собой структуру типа <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4acfc-142">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4acfc-143">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="4acfc-143">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="4acfc-144">Код региона запрашивает определение региона, которое может играть декодер, в соответствии с определением в консорциуме DVD.</span><span class="sxs-lookup"><span data-stu-id="4acfc-144">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="4acfc-145">Этот регион определен как структура <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4acfc-145">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4acfc-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="4acfc-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="4acfc-147">В этом свойстве поддерживаются оба варианта: Get и Set.</span><span class="sxs-lookup"><span data-stu-id="4acfc-147">Both get and set are supported on this property.</span></span> <span data-ttu-id="4acfc-148">Сначала вызывается метод Get, чтобы определить, требуется ли проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="4acfc-148">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="4acfc-149">Свойства набора указывают на фазу согласования защиты копирования, которую вводит фильтр.</span><span class="sxs-lookup"><span data-stu-id="4acfc-149">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="4acfc-150">Передаваемые данные будут представлять собой структуру типа <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4acfc-150">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4acfc-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="4acfc-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="4acfc-152">Если это свойство имеет <strong>значение true</strong>, Навигатор DVD не отправляет образцы <strong>AM_UseNewCSSKey</strong> перед согласованием ключа диска.</span><span class="sxs-lookup"><span data-stu-id="4acfc-152">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="4acfc-153">См. <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4acfc-153">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="4acfc-154">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4acfc-154">Read-only.</span></span> <span data-ttu-id="4acfc-155">Данные свойства являются <strong>логическим</strong> значением.</span><span class="sxs-lookup"><span data-stu-id="4acfc-155">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4acfc-156">Применяется к Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4acfc-156">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4acfc-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="4acfc-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="4acfc-158">Это свойство только для установки.</span><span class="sxs-lookup"><span data-stu-id="4acfc-158">This is a set-only property.</span></span> <span data-ttu-id="4acfc-159">Он предоставляет ключ заголовка из текущего содержимого.</span><span class="sxs-lookup"><span data-stu-id="4acfc-159">This provides title key from current content.</span></span> <span data-ttu-id="4acfc-160">Ключ представляет собой структуру типа <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4acfc-160">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="4acfc-161">Требования</span><span class="sxs-lookup"><span data-stu-id="4acfc-161">Requirements</span></span>



| <span data-ttu-id="4acfc-162">Требование</span><span class="sxs-lookup"><span data-stu-id="4acfc-162">Requirement</span></span> | <span data-ttu-id="4acfc-163">Значение</span><span class="sxs-lookup"><span data-stu-id="4acfc-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4acfc-164">Header</span><span class="sxs-lookup"><span data-stu-id="4acfc-164">Header</span></span><br/> | <dl> <span data-ttu-id="4acfc-165"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="4acfc-165"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4acfc-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4acfc-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4acfc-167">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="4acfc-167">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




