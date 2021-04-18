---
title: Структура WINBIO_BIR_HEADER (Винбио \_ types. h)
description: Содержит заголовок записи биометрической информации (Бир).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- API структуры WINBIO_BIR_HEADER биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135911"
---
# <a name="winbio_bir_header-structure"></a><span data-ttu-id="e36ce-104">\_ \_ Структура заголовка винбио Бир</span><span class="sxs-lookup"><span data-stu-id="e36ce-104">WINBIO\_BIR\_HEADER structure</span></span>

<span data-ttu-id="e36ce-105">Структура **\_ \_ заголовка винбио Бир** содержит заголовок записи биометрической информации (Бир).</span><span class="sxs-lookup"><span data-stu-id="e36ce-105">The **WINBIO\_BIR\_HEADER** structure contains the header of a biometric information record (BIR).</span></span>

## <a name="syntax"></a><span data-ttu-id="e36ce-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e36ce-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a><span data-ttu-id="e36ce-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e36ce-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e36ce-108">**валидфиелдс**</span><span class="sxs-lookup"><span data-stu-id="e36ce-108">**ValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-109">Битовая маска, указывающая, какие поля в этой структуре являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="e36ce-109">Bitmask that specifies which fields in this structure are valid.</span></span> <span data-ttu-id="e36ce-110">Дополнительные сведения см. в [**разделе \_ \_ константы поля винбио Бир**](winbio-bir-field-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e36ce-110">For more information, see [**WINBIO\_BIR\_FIELD Constants**](winbio-bir-field-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-111">**HeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="e36ce-111">**HeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-112">Константа **\_ \_ версии Бир винбио** , указывающая версию заголовка.</span><span class="sxs-lookup"><span data-stu-id="e36ce-112">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="e36ce-113">Номера версий — это 8-разрядные значения, где четыре верхних бита указывают основной номер, а младшие четыре бита указывают дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="e36ce-113">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="e36ce-114">В настоящее время это должна \_ быть \_ версия винбио кбефф Header \_ (0x11).</span><span class="sxs-lookup"><span data-stu-id="e36ce-114">Currently this must be WINBIO\_CBEFF\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-115">**патронхеадерверсион**</span><span class="sxs-lookup"><span data-stu-id="e36ce-115">**PatronHeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-116">Константа **\_ \_ версии Бир винбио** , указывающая версию заголовка.</span><span class="sxs-lookup"><span data-stu-id="e36ce-116">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="e36ce-117">Номера версий — это 8-разрядные значения, где четыре верхних бита указывают основной номер, а младшие четыре бита указывают дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="e36ce-117">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="e36ce-118">В настоящее время это должна \_ быть \_ версия винбио патрон Header \_ (0x11).</span><span class="sxs-lookup"><span data-stu-id="e36ce-118">Currently this must be WINBIO\_PATRON\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-119">**Флаги.**</span><span class="sxs-lookup"><span data-stu-id="e36ce-119">**DataFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-120">Значение типа, указывающее формат данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="e36ce-120">A value that specifies the format of the header data.</span></span> <span data-ttu-id="e36ce-121">Это может быть побитовое **или** для следующих флагов безопасности и уровня обработки.</span><span class="sxs-lookup"><span data-stu-id="e36ce-121">This can be a bitwise **OR** of the following security and processing level flags.</span></span> <span data-ttu-id="e36ce-122">Дополнительные сведения см. в [**разделе \_ \_ константы винбио Бир Data \_ flags**](winbio-bir-data-flags-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e36ce-122">For more information, see [**WINBIO\_BIR\_DATA\_FLAGS Constants**](winbio-bir-data-flags-constants.md).</span></span>



| <span data-ttu-id="e36ce-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e36ce-123">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="e36ce-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e36ce-124">Meaning</span></span>                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="e36ce-125"><dt>**Винбио \_ \_ \_ Конфиденциальность флага данных**</dt> <dt>((Учар) 0x02)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-125"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>((UCHAR)0x02)</dt></span></span> </dl>                                       | <span data-ttu-id="e36ce-126">Данные зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="e36ce-126">The data is encrypted.</span></span><br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="e36ce-127"><dt>**Винбио \_ \_ \_ Целостность флагов данных**</dt> <dt>((Учар) 0x01)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-127"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>((UCHAR)0x01)</dt></span></span> </dl>                                 | <span data-ttu-id="e36ce-128">Данные имеют цифровую подпись или защищаются с помощью кода проверки подлинности сообщений (MAC).</span><span class="sxs-lookup"><span data-stu-id="e36ce-128">The data is digitally signed or protected by a message authentication code (MAC).</span></span><br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="e36ce-129"><dt>**Винбио \_ \_ \_ Подписанный флаг данных**</dt> <dt>((Учар) 0x04)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-129"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>((UCHAR)0x04)</dt></span></span> </dl>                                          | <span data-ttu-id="e36ce-130">Если установлен этот флаг и **флаг \_ \_ \_ целостности флага данных винбио** , данные подписываются.</span><span class="sxs-lookup"><span data-stu-id="e36ce-130">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="e36ce-131">Если этот флаг не установлен, но установлен **флаг \_ \_ \_ целостности флага данных винбио** , то для данных будет вычисляться Mac-адрес.</span><span class="sxs-lookup"><span data-stu-id="e36ce-131">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed over the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="e36ce-132"><dt>**Винбио \_ \_Флаг данных \_ RAW**</dt> <dt>((Учар) 0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-132"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>((UCHAR)0x20)</dt></span></span> </dl>                                                   | <span data-ttu-id="e36ce-133">Данные имеют формат, с которым они были захвачены.</span><span class="sxs-lookup"><span data-stu-id="e36ce-133">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="e36ce-134"><dt>**Винбио \_ \_ \_ Промежуточный флаг данных**</dt> <dt>((Учар) 0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-134"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt></span></span> </dl>                        | <span data-ttu-id="e36ce-135">Данные не являются необработанными, но обработаны не полностью.</span><span class="sxs-lookup"><span data-stu-id="e36ce-135">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="e36ce-136"><dt>**Винбио \_ \_ \_ Обработанный флаг данных**</dt> <dt>((Учар) 0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-136"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>((UCHAR)0x80)</dt></span></span> </dl>                                 | <span data-ttu-id="e36ce-137">Данные обработаны.</span><span class="sxs-lookup"><span data-stu-id="e36ce-137">The data has been processed.</span></span><br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="e36ce-138"><dt>**Винбио \_ \_Маска параметра флага данных \_ \_ \_ имеется**</dt> <dt>((Учар) 0x08)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-138"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>((UCHAR)0x08)</dt></span></span> </dl> | <span data-ttu-id="e36ce-139">Это значение всегда равно 1.</span><span class="sxs-lookup"><span data-stu-id="e36ce-139">This value is always 1.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="e36ce-140">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e36ce-140">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-141">Значение биометрического \_ \_ типа винбио, которое указывает тип биометрических данных, на которые ссылается запись биометрической информации.</span><span class="sxs-lookup"><span data-stu-id="e36ce-141">A WINBIO\_BIOMETRIC\_TYPE value that specifies the type of biometric data referenced in the biometric information record.</span></span> <span data-ttu-id="e36ce-142">В настоящее время поддерживается только **\_ \_ отпечаток типа винбио** .</span><span class="sxs-lookup"><span data-stu-id="e36ce-142">Currently only **WINBIO\_TYPE\_FINGERPRINT** is supported.</span></span> <span data-ttu-id="e36ce-143">Дополнительные сведения см. в [**разделе \_ \_ КОНСТАНТы биометрического типа винбио**](winbio-biometric-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e36ce-143">For more information, see [**WINBIO\_BIOMETRIC\_TYPE Constants**](winbio-biometric-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-144">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="e36ce-144">**Subtype**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-145">Значение **\_ \_ ПОДтипа БИОметрической метрики винбио** , указывающее вспомогательный фактор, связанный с биометрических данными.</span><span class="sxs-lookup"><span data-stu-id="e36ce-145">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="e36ce-146">Дополнительные сведения см. в разделе remarks and [**винбио \_ биометрические \_ константы подтипа**](winbio-biometric-subtype-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e36ce-146">For more information, see Remarks and [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-147">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="e36ce-147">**Purpose**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-148">Маска **\_ \_ цели Бир винбио** , которая указывает предполагаемое использование данных.</span><span class="sxs-lookup"><span data-stu-id="e36ce-148">A **WINBIO\_BIR\_PURPOSE** mask that specifies the intended use of the data.</span></span> <span data-ttu-id="e36ce-149">Это может быть побитовое **или** из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e36ce-149">This can be a bitwise **OR** of the following values.</span></span> <span data-ttu-id="e36ce-150">Дополнительные сведения см. в статье [**винбио \_ Бир \_ назначение констант**](winbio-bir-purpose-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e36ce-150">For more information, see [**WINBIO\_BIR\_PURPOSE Constants**](winbio-bir-purpose-constants.md).</span></span>

-   <span data-ttu-id="e36ce-151">\_Проверка цели \_ винбио</span><span class="sxs-lookup"><span data-stu-id="e36ce-151">WINBIO\_PURPOSE\_VERIFY</span></span>
-   <span data-ttu-id="e36ce-152">\_назначение винбио \_</span><span class="sxs-lookup"><span data-stu-id="e36ce-152">WINBIO\_PURPOSE\_IDENTIFY</span></span>
-   <span data-ttu-id="e36ce-153">\_Регистрация цели \_ винбио</span><span class="sxs-lookup"><span data-stu-id="e36ce-153">WINBIO\_PURPOSE\_ENROLL</span></span>
-   <span data-ttu-id="e36ce-154">ВИНБИО \_ цель \_ регистрации \_ для \_ проверки</span><span class="sxs-lookup"><span data-stu-id="e36ce-154">WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION</span></span>
-   <span data-ttu-id="e36ce-155">\_Регистрация назначения \_ винбио \_ для \_ идентификации</span><span class="sxs-lookup"><span data-stu-id="e36ce-155">WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION</span></span>
-   <span data-ttu-id="e36ce-156">\_Аудит назначения \_ винбио</span><span class="sxs-lookup"><span data-stu-id="e36ce-156">WINBIO\_PURPOSE\_AUDIT</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-157">**Качество передачи**</span><span class="sxs-lookup"><span data-stu-id="e36ce-157">**DataQuality**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-158">Значение, указывающее относительное качество биометрических данных в записи биометрической информации (Бир).</span><span class="sxs-lookup"><span data-stu-id="e36ce-158">A value that specifies the relative quality of the biometric data in the biometric information record (BIR).</span></span> <span data-ttu-id="e36ce-159">Это может быть целое число от 0 до 100 или одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e36ce-159">This can be an integer from 0 to 100 or one of the following values.</span></span> <span data-ttu-id="e36ce-160">Дополнительные сведения см. в разделе [**винбио \_ Бир \_ Quality константы**](winbio-bir-quality-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e36ce-160">For more information, see [**WINBIO\_BIR\_QUALITY Constants**](winbio-bir-quality-constants.md).</span></span>



| <span data-ttu-id="e36ce-161">Значение</span><span class="sxs-lookup"><span data-stu-id="e36ce-161">Value</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="e36ce-162">Значение</span><span class="sxs-lookup"><span data-stu-id="e36ce-162">Meaning</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="e36ce-163"><dt>**Винбио \_ \_Качество данных \_ не \_ задано**</dt> <dt>((винбио \_ Бир \_ Quality)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-163"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt>((WINBIO\_BIR\_QUALITY)-1)</dt></span></span> </dl>                   | <span data-ttu-id="e36ce-164">Измерения качества поддерживаются создателем Бир, но в Бир не задано значение.</span><span class="sxs-lookup"><span data-stu-id="e36ce-164">Quality measurements are supported by the BIR creator but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="e36ce-165"><dt>**Винбио \_ \_Качество данных \_ не \_ поддерживается**</dt> <dt>((винбио \_ Бир \_ Quality)-2)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-165"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt>((WINBIO\_BIR\_QUALITY)-2)</dt></span></span> </dl> | <span data-ttu-id="e36ce-166">Измерения качества не поддерживаются создателем Бир.</span><span class="sxs-lookup"><span data-stu-id="e36ce-166">Quality measurements are not supported by the BIR creator.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="e36ce-167">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="e36ce-167">**CreationDate**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-168">Дата и время создания Бир в формате всемирного координированного времени (время по Гринвичу).</span><span class="sxs-lookup"><span data-stu-id="e36ce-168">The date and time, in Coordinated Universal Time (Greenwich Mean Time), that the BIR was created.</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-169">**ValidityPeriod**</span><span class="sxs-lookup"><span data-stu-id="e36ce-169">**ValidityPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-170">Период, для которого Бир является допустимым.</span><span class="sxs-lookup"><span data-stu-id="e36ce-170">The period for which the BIR is valid.</span></span>

<dl> <dt>

<span data-ttu-id="e36ce-171">**BeginDate**</span><span class="sxs-lookup"><span data-stu-id="e36ce-171">**BeginDate**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-172">Дата и время начала периода действия в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="e36ce-172">The date and time, in Coordinated Universal Time, that the validity period starts.</span></span>

</dd> <dt>

<span data-ttu-id="e36ce-173">**Предшеству**</span><span class="sxs-lookup"><span data-stu-id="e36ce-173">**EndDate**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-174">Дата и время (в формате UTC), в течение которых Бир перестает быть допустимым.</span><span class="sxs-lookup"><span data-stu-id="e36ce-174">The date and time, in Coordinated Universal Time, at which the BIR ceases to be valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e36ce-175">**биометрикдатаформат**</span><span class="sxs-lookup"><span data-stu-id="e36ce-175">**BiometricDataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-176">[**Винбио \_ зарегистрированная структура \_ формата**](winbio-registered-format.md) , указывающая формат данных стандартного блока данных в структуре [**винбио \_ Бир**](winbio-bir.md) .</span><span class="sxs-lookup"><span data-stu-id="e36ce-176">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the data format of the standard data block in the [**WINBIO\_BIR**](winbio-bir.md) structure.</span></span> <span data-ttu-id="e36ce-177">**\_ Зарегистрированные элементы \_ формата винбио** не могут быть равны нулю.</span><span class="sxs-lookup"><span data-stu-id="e36ce-177">The **WINBIO\_REGISTERED\_FORMAT** members cannot be zero.</span></span> <span data-ttu-id="e36ce-178">Для упрощения проверки ошибок можно использовать следующие константы.</span><span class="sxs-lookup"><span data-stu-id="e36ce-178">You can use the following constants to simplify error checking.</span></span>



| <span data-ttu-id="e36ce-179">Значение</span><span class="sxs-lookup"><span data-stu-id="e36ce-179">Value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="e36ce-180">Значение</span><span class="sxs-lookup"><span data-stu-id="e36ce-180">Meaning</span></span>                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <span data-ttu-id="e36ce-181"><dt>**Винбио \_ НЕТ \_ \_ \_ доступного владельца формата**</dt> <dt>((UShort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-181"><dt>**WINBIO\_NO\_FORMAT\_OWNER\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl> | <span data-ttu-id="e36ce-182">Не указано значение владельца ИБИА (Международная биометрическая Ассоциация отрасли).</span><span class="sxs-lookup"><span data-stu-id="e36ce-182">No IBIA (International Biometric Industry Association) assigned owner value has been specified.</span></span><br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <span data-ttu-id="e36ce-183"><dt>**Винбио \_ НЕТ \_ \_ \_ доступного типа формата**</dt> <dt>((UShort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-183"><dt>**WINBIO\_NO\_FORMAT\_TYPE\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl>    | <span data-ttu-id="e36ce-184">Не указан тип формата.</span><span class="sxs-lookup"><span data-stu-id="e36ce-184">No format type has been specified.</span></span><br/>                                                              |



 

</dd> <dt>

<span data-ttu-id="e36ce-185">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="e36ce-185">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="e36ce-186">[**Винбио \_ зарегистрированная структура \_ формата**](winbio-registered-format.md) , указывающая идентификатор продукта компонента, создавшего Стандартный блок данных в Бир.</span><span class="sxs-lookup"><span data-stu-id="e36ce-186">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the product ID of the component that generated the standard data block in the BIR.</span></span> <span data-ttu-id="e36ce-187">**\_ Зарегистрированные элементы \_ формата винбио** могут быть равны нулю.</span><span class="sxs-lookup"><span data-stu-id="e36ce-187">The **WINBIO\_REGISTERED\_FORMAT** members can be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e36ce-188">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e36ce-188">Remarks</span></span>

<span data-ttu-id="e36ce-189">Параметр *подтипа* указывает вспомогательный фактор, связанный с биометрических данными.</span><span class="sxs-lookup"><span data-stu-id="e36ce-189">The *Subtype* parameter specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="e36ce-190">В настоящее время биометрическая платформа Windows (ВБФ) поддерживает только захват отпечатков пальцев и использует следующие константы для представления сведений о подтипах:</span><span class="sxs-lookup"><span data-stu-id="e36ce-190">Currently, the Windows Biometric Framework (WBF) supports only fingerprint capture and uses the following constants to represent sub-type information:</span></span>

-   <span data-ttu-id="e36ce-191">ВИНБИО \_ ANSI \_ 381 \_ POS \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="e36ce-191">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="e36ce-192">ВИНБИО \_ ANSI \_ 381 \_ \_ RH POS \_</span><span class="sxs-lookup"><span data-stu-id="e36ce-192">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="e36ce-193">ВИНБИО \_ \_ \_ \_ RH \_ указатель \_ пальца ANSI 381 POS</span><span class="sxs-lookup"><span data-stu-id="e36ce-193">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="e36ce-194">ВИНБИО \_ ANSI \_ 381 \_ \_ RH, \_ средний \_ палец</span><span class="sxs-lookup"><span data-stu-id="e36ce-194">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="e36ce-195">ВИНБИО \_ ANSI \_ 381 \_ POS \_ RH \_ Ring \_</span><span class="sxs-lookup"><span data-stu-id="e36ce-195">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="e36ce-196">ВИНБИО \_ ANSI \_ 381 \_ \_ RH, \_ маленький \_ палец</span><span class="sxs-lookup"><span data-stu-id="e36ce-196">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="e36ce-197">ВИНБИОный \_ \_ \_ \_ бегунок ANSI 381 POS \_</span><span class="sxs-lookup"><span data-stu-id="e36ce-197">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="e36ce-198">ВИНБИОный \_ палец с индексами в формате ANSI \_ 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="e36ce-198">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="e36ce-199">\_ \_ Средний палец винбио ANSI 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="e36ce-199">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="e36ce-200">ВИНБИОный \_ палец в формате ANSI \_ 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="e36ce-200">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="e36ce-201">ВИНБИО \_ ANSI \_ 381 \_ POS \_ , \_ маленький \_ палец</span><span class="sxs-lookup"><span data-stu-id="e36ce-201">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="e36ce-202">ВИНБИО \_ ANSI \_ 381 \_ RH POS с \_ \_ четырьмя \_ пальцами</span><span class="sxs-lookup"><span data-stu-id="e36ce-202">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="e36ce-203">ВИНБИО \_ ANSI \_ 381 \_ POS \_ LH \_ четыре \_ пальца</span><span class="sxs-lookup"><span data-stu-id="e36ce-203">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="e36ce-204">ВИНБИО \_ ANSI \_ 381 \_ POS \_ 2 \_ Thumbs</span><span class="sxs-lookup"><span data-stu-id="e36ce-204">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e36ce-205">Не пытайтесь проверить значение, заданное для значения параметра *подтипа* .</span><span class="sxs-lookup"><span data-stu-id="e36ce-205">Do not attempt to validate the value supplied for the *Subtype* parameter value.</span></span> <span data-ttu-id="e36ce-206">Служба биометрических систем Windows проверит переданное значение перед его передачей в реализацию.</span><span class="sxs-lookup"><span data-stu-id="e36ce-206">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="e36ce-207">Если значение **винбио \_ подтипа \_ нет \_ данных** или **винбио \_ подтип \_ ANY**, то проверьте, где это необходимо.</span><span class="sxs-lookup"><span data-stu-id="e36ce-207">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

<span data-ttu-id="e36ce-208">При утверждении любого из следующих битов структура **\_ \_ заголовка винбио Бир** неправильно сформирована.</span><span class="sxs-lookup"><span data-stu-id="e36ce-208">If any of the following bits are asserted, the **WINBIO\_BIR\_HEADER** structure is not correctly formed.</span></span>


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a><span data-ttu-id="e36ce-209">Требования</span><span class="sxs-lookup"><span data-stu-id="e36ce-209">Requirements</span></span>



| <span data-ttu-id="e36ce-210">Требование</span><span class="sxs-lookup"><span data-stu-id="e36ce-210">Requirement</span></span> | <span data-ttu-id="e36ce-211">Значение</span><span class="sxs-lookup"><span data-stu-id="e36ce-211">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e36ce-212">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e36ce-212">Minimum supported client</span></span><br/> | <span data-ttu-id="e36ce-213">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-213">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e36ce-214">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e36ce-214">Minimum supported server</span></span><br/> | <span data-ttu-id="e36ce-215">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e36ce-215">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e36ce-216">Header</span><span class="sxs-lookup"><span data-stu-id="e36ce-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="e36ce-217"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e36ce-217"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e36ce-218">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e36ce-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e36ce-219">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="e36ce-219">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="e36ce-220">**\_Константы ПОДтипа БИОметрической метрики винбио \_**</span><span class="sxs-lookup"><span data-stu-id="e36ce-220">**WINBIO\_BIOMETRIC\_SUBTYPE Constants**</span></span>](winbio-biometric-subtype-constants.md)
</dt> <dt>

[<span data-ttu-id="e36ce-221">**ВИНБИО \_ Бир**</span><span class="sxs-lookup"><span data-stu-id="e36ce-221">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="e36ce-222">**\_ \_ \_ Константы флагов данных винбио Бир**</span><span class="sxs-lookup"><span data-stu-id="e36ce-222">**WINBIO\_BIR\_DATA\_FLAGS Constants**</span></span>](winbio-bir-data-flags-constants.md)
</dt> <dt>

[<span data-ttu-id="e36ce-223">**\_ \_ Константы поля винбио Бир**</span><span class="sxs-lookup"><span data-stu-id="e36ce-223">**WINBIO\_BIR\_FIELD Constants**</span></span>](winbio-bir-field-constants.md)
</dt> <dt>

[<span data-ttu-id="e36ce-224">**\_ \_ Константы назначения Бир винбио**</span><span class="sxs-lookup"><span data-stu-id="e36ce-224">**WINBIO\_BIR\_PURPOSE Constants**</span></span>](winbio-bir-purpose-constants.md)
</dt> <dt>

[<span data-ttu-id="e36ce-225">**\_ \_ Константы качества винбио Бир**</span><span class="sxs-lookup"><span data-stu-id="e36ce-225">**WINBIO\_BIR\_QUALITY Constants**</span></span>](winbio-bir-quality-constants.md)
</dt> <dt>

[<span data-ttu-id="e36ce-226">**\_ \_ Константы версии Бир винбио**</span><span class="sxs-lookup"><span data-stu-id="e36ce-226">**WINBIO\_BIR\_VERSION Constants**</span></span>](winbio-bir-version-constants.md)
</dt> </dl>

 

 





