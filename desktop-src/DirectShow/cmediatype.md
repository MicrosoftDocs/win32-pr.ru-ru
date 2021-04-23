---
description: Класс Кмедиатипе управляет типами мультимедиа. Этот класс наследует \_ \_ структуру типа мультимедиа AM. Его можно привести к переменным типа \_ Media \_ Type.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Класс Кмедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665500"
---
# <a name="cmediatype-class"></a><span data-ttu-id="915c6-105">Класс Кмедиатипе</span><span class="sxs-lookup"><span data-stu-id="915c6-105">CMediaType class</span></span>

![Иерархия классов кмедиатипе](images/mtype01.png)

<span data-ttu-id="915c6-107">`CMediaType`Класс управляет типами мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="915c6-107">The `CMediaType` class manages media types.</span></span> <span data-ttu-id="915c6-108">Этот класс наследует структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="915c6-108">This class inherits the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="915c6-109">Его можно привести к переменным типа **\_ Media \_ Type**.</span><span class="sxs-lookup"><span data-stu-id="915c6-109">It can be cast to a variable of type **AM\_MEDIA\_TYPE**.</span></span>



| <span data-ttu-id="915c6-110">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="915c6-110">Public Methods</span></span>                                                      | <span data-ttu-id="915c6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="915c6-111">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="915c6-112">**кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="915c6-112">**CMediaType**</span></span>](cmediatype-cmediatype.md)                         | <span data-ttu-id="915c6-113">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="915c6-113">Constructor method.</span></span>                                                            |
| [<span data-ttu-id="915c6-114">**~ Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="915c6-114">**~CMediaType**</span></span>](cmediatype--cmediatype.md)                       | <span data-ttu-id="915c6-115">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="915c6-115">Destructor method.</span></span>                                                             |
| [<span data-ttu-id="915c6-116">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="915c6-116">**Set**</span></span>](cmediatype-set.md)                                       | <span data-ttu-id="915c6-117">Задает тип носителя с другого типа носителя.</span><span class="sxs-lookup"><span data-stu-id="915c6-117">Sets the media type from another media type.</span></span>                                   |
| [<span data-ttu-id="915c6-118">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="915c6-118">**IsValid**</span></span>](cmediatype-isvalid.md)                               | <span data-ttu-id="915c6-119">Определяет, был ли присвоен основной тип этому объекту.</span><span class="sxs-lookup"><span data-stu-id="915c6-119">Determines whether a major type has been assigned to this object.</span></span>              |
| [<span data-ttu-id="915c6-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="915c6-120">**Type**</span></span>](cmediatype-type.md)                                     | <span data-ttu-id="915c6-121">Извлекает основной тип.</span><span class="sxs-lookup"><span data-stu-id="915c6-121">Retrieves the major type.</span></span>                                                      |
| [<span data-ttu-id="915c6-122">**сеттипе**</span><span class="sxs-lookup"><span data-stu-id="915c6-122">**SetType**</span></span>](cmediatype-settype.md)                               | <span data-ttu-id="915c6-123">Указывает основной тип.</span><span class="sxs-lookup"><span data-stu-id="915c6-123">Specifies the major type.</span></span>                                                      |
| [<span data-ttu-id="915c6-124">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="915c6-124">**Subtype**</span></span>](cmediatype-subtype.md)                               | <span data-ttu-id="915c6-125">Извлекает подтип.</span><span class="sxs-lookup"><span data-stu-id="915c6-125">Retrieves the subtype.</span></span>                                                         |
| [<span data-ttu-id="915c6-126">**сетсубтипе**</span><span class="sxs-lookup"><span data-stu-id="915c6-126">**SetSubtype**</span></span>](cmediatype-setsubtype.md)                         | <span data-ttu-id="915c6-127">Указывает подтип.</span><span class="sxs-lookup"><span data-stu-id="915c6-127">Specifies the subtype.</span></span>                                                         |
| [<span data-ttu-id="915c6-128">**IsFixedSize**</span><span class="sxs-lookup"><span data-stu-id="915c6-128">**IsFixedSize**</span></span>](cmediatype-isfixedsize.md)                       | <span data-ttu-id="915c6-129">Определяет, имеют ли образцы фиксированный размер или переменный размер.</span><span class="sxs-lookup"><span data-stu-id="915c6-129">Determines if the samples have a fixed size or a variable size.</span></span>                |
| [<span data-ttu-id="915c6-130">**истемпоралкомпрессед**</span><span class="sxs-lookup"><span data-stu-id="915c6-130">**IsTemporalCompressed**</span></span>](cmediatype-istemporalcompressed.md)     | <span data-ttu-id="915c6-131">Определяет, использует ли поток временное сжатие.</span><span class="sxs-lookup"><span data-stu-id="915c6-131">Determines if the stream uses temporal compression.</span></span>                            |
| [<span data-ttu-id="915c6-132">**жетсамплесизе**</span><span class="sxs-lookup"><span data-stu-id="915c6-132">**GetSampleSize**</span></span>](cmediatype-getsamplesize.md)                   | <span data-ttu-id="915c6-133">Получает размер выборки.</span><span class="sxs-lookup"><span data-stu-id="915c6-133">Retrieves the sample size.</span></span>                                                     |
| [<span data-ttu-id="915c6-134">**сетсамплесизе**</span><span class="sxs-lookup"><span data-stu-id="915c6-134">**SetSampleSize**</span></span>](cmediatype-setsamplesize.md)                   | <span data-ttu-id="915c6-135">Задает фиксированный размер выборки или указывает, что выборки имеют переменный размер.</span><span class="sxs-lookup"><span data-stu-id="915c6-135">Specifies a fixed sample size, or specifies that samples have a variable size.</span></span> |
| [<span data-ttu-id="915c6-136">**сетвариаблесизе**</span><span class="sxs-lookup"><span data-stu-id="915c6-136">**SetVariableSize**</span></span>](cmediatype-setvariablesize.md)               | <span data-ttu-id="915c6-137">Указывает, что выборки не имеют фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="915c6-137">Specifies that samples do not have a fixed size.</span></span>                               |
| [<span data-ttu-id="915c6-138">**сеттемпоралкомпрессион**</span><span class="sxs-lookup"><span data-stu-id="915c6-138">**SetTemporalCompression**</span></span>](cmediatype-settemporalcompression.md) | <span data-ttu-id="915c6-139">Указывает, сжимаются ли образцы с использованием временного сжатия.</span><span class="sxs-lookup"><span data-stu-id="915c6-139">Specifies whether samples are compressed using temporal compression.</span></span>           |
| [<span data-ttu-id="915c6-140">**Формат**</span><span class="sxs-lookup"><span data-stu-id="915c6-140">**Format**</span></span>](cmediatype-format.md)                                 | <span data-ttu-id="915c6-141">Получает указатель на блок формата.</span><span class="sxs-lookup"><span data-stu-id="915c6-141">Retrieves a pointer to the format block.</span></span>                                       |
| [<span data-ttu-id="915c6-142">**форматленгс**</span><span class="sxs-lookup"><span data-stu-id="915c6-142">**FormatLength**</span></span>](cmediatype-formatlength.md)                     | <span data-ttu-id="915c6-143">Получает длину блока форматирования.</span><span class="sxs-lookup"><span data-stu-id="915c6-143">Retrieves the length of the format block.</span></span>                                      |
| [<span data-ttu-id="915c6-144">**сетформаттипе**</span><span class="sxs-lookup"><span data-stu-id="915c6-144">**SetFormatType**</span></span>](cmediatype-setformattype.md)                   | <span data-ttu-id="915c6-145">Определяет тип формата.</span><span class="sxs-lookup"><span data-stu-id="915c6-145">Specifies the format type.</span></span>                                                     |
| [<span data-ttu-id="915c6-146">**форматтипе**</span><span class="sxs-lookup"><span data-stu-id="915c6-146">**FormatType**</span></span>](cmediatype-formattype.md)                         | <span data-ttu-id="915c6-147">Возвращает тип формата.</span><span class="sxs-lookup"><span data-stu-id="915c6-147">Retrieves the format type.</span></span>                                                     |
| [<span data-ttu-id="915c6-148">**сетформат**</span><span class="sxs-lookup"><span data-stu-id="915c6-148">**SetFormat**</span></span>](cmediatype-setformat.md)                           | <span data-ttu-id="915c6-149">Задает блок формата.</span><span class="sxs-lookup"><span data-stu-id="915c6-149">Specifies the format block.</span></span>                                                    |
| [<span data-ttu-id="915c6-150">**ресетформатбуффер**</span><span class="sxs-lookup"><span data-stu-id="915c6-150">**ResetFormatBuffer**</span></span>](cmediatype-resetformatbuffer.md)           | <span data-ttu-id="915c6-151">Удаляет блок формата.</span><span class="sxs-lookup"><span data-stu-id="915c6-151">Deletes the format block.</span></span>                                                      |
| [<span data-ttu-id="915c6-152">**аллокформатбуффер**</span><span class="sxs-lookup"><span data-stu-id="915c6-152">**AllocFormatBuffer**</span></span>](cmediatype-allocformatbuffer.md)           | <span data-ttu-id="915c6-153">Выделяет память для блока Format.</span><span class="sxs-lookup"><span data-stu-id="915c6-153">Allocates memory for the format block.</span></span>                                         |
| [<span data-ttu-id="915c6-154">**реаллокформатбуффер**</span><span class="sxs-lookup"><span data-stu-id="915c6-154">**ReallocFormatBuffer**</span></span>](cmediatype-reallocformatbuffer.md)       | <span data-ttu-id="915c6-155">Перераспределяет блок формата на новый размер.</span><span class="sxs-lookup"><span data-stu-id="915c6-155">Reallocates the format block to a new size.</span></span>                                    |
| [<span data-ttu-id="915c6-156">**инитмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="915c6-156">**InitMediaType**</span></span>](cmediatype-initmediatype.md)                   | <span data-ttu-id="915c6-157">Инициализирует тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="915c6-157">Initializes the media type.</span></span>                                                    |
| [<span data-ttu-id="915c6-158">**матчеспартиал**</span><span class="sxs-lookup"><span data-stu-id="915c6-158">**MatchesPartial**</span></span>](cmediatype-matchespartial.md)                 | <span data-ttu-id="915c6-159">Определяет, соответствует ли этот тип носителя частично указанному типу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="915c6-159">Determines if this media type matches a partially specified media type.</span></span>        |
| [<span data-ttu-id="915c6-160">**испартиаллиспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="915c6-160">**IsPartiallySpecified**</span></span>](cmediatype-ispartiallyspecified.md)     | <span data-ttu-id="915c6-161">Определяет, определен ли тип мультимедиа частично.</span><span class="sxs-lookup"><span data-stu-id="915c6-161">Determines if the media type is partially defined.</span></span>                             |
| <span data-ttu-id="915c6-162">Операторы</span><span class="sxs-lookup"><span data-stu-id="915c6-162">Operators</span></span>                                                           | <span data-ttu-id="915c6-163">Описание:</span><span class="sxs-lookup"><span data-stu-id="915c6-163">Description</span></span>                                                                    |
| [<span data-ttu-id="915c6-164">**Оператор =**</span><span class="sxs-lookup"><span data-stu-id="915c6-164">**operator =**</span></span>](cmediatype-operator-.md)                          | <span data-ttu-id="915c6-165">Перегружает оператор присваивания для копирования типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="915c6-165">Overloads the assignment operator to copy a media type.</span></span>                        |
| [<span data-ttu-id="915c6-166">**Оператор = =**</span><span class="sxs-lookup"><span data-stu-id="915c6-166">**operator ==**</span></span>](cmediatype-operator--.md)                        | <span data-ttu-id="915c6-167">Проверяет равенство между объектами `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="915c6-167">Tests for equality between `CMediaType` objects.</span></span>                               |
| [<span data-ttu-id="915c6-168">**operator! =**</span><span class="sxs-lookup"><span data-stu-id="915c6-168">**operator !=**</span></span>](cmediatype-operator-neq.md)                      | <span data-ttu-id="915c6-169">Проверяет неравенство между объектами `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="915c6-169">Tests for inequality between `CMediaType` objects.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="915c6-170">Требования</span><span class="sxs-lookup"><span data-stu-id="915c6-170">Requirements</span></span>



| <span data-ttu-id="915c6-171">Требование</span><span class="sxs-lookup"><span data-stu-id="915c6-171">Requirement</span></span> | <span data-ttu-id="915c6-172">Значение</span><span class="sxs-lookup"><span data-stu-id="915c6-172">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="915c6-173">Header</span><span class="sxs-lookup"><span data-stu-id="915c6-173">Header</span></span><br/>  | <dl> <span data-ttu-id="915c6-174"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="915c6-174"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="915c6-175">Библиотека</span><span class="sxs-lookup"><span data-stu-id="915c6-175">Library</span></span><br/> | <dl> <span data-ttu-id="915c6-176"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="915c6-176"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




