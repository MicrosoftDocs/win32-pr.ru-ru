---
description: Значение, указывающее размер (в байтах) типа объекта метаданных пространственного аудио, который будет выводиться декодером.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: Атрибут MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264750"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a><span data-ttu-id="88726-103">\_ \_ \_ \_ \_ Атрибут длины метаданных объекта пространственного звука \_ MF MT</span><span class="sxs-lookup"><span data-stu-id="88726-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_LENGTH attribute</span></span>

<span data-ttu-id="88726-104">Значение, указывающее размер (в байтах) типа объекта метаданных пространственного аудио, который будет выводиться декодером.</span><span class="sxs-lookup"><span data-stu-id="88726-104">A value specifying the size, in bytes, of the spatial audio metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="88726-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="88726-105">Data type</span></span>

<span data-ttu-id="88726-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="88726-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="88726-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88726-107">Remarks</span></span>

<span data-ttu-id="88726-108">Большой двоичный объект метаданных с указанным форматом записывается с помощью интерфейса [**испатиалаудиометадатавритер**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) и считывается с помощью интерфейса [**испатиалаудиометадатареадер**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="88726-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="88726-109">Большой двоичный объект метаданных непрозрачен для Media Foundation конвейера и компонентов.</span><span class="sxs-lookup"><span data-stu-id="88726-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="88726-110">Атрибут применяется к типу пространственного звукового носителя.</span><span class="sxs-lookup"><span data-stu-id="88726-110">The attribute is applied to the spatial audio media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="88726-111">Требования</span><span class="sxs-lookup"><span data-stu-id="88726-111">Requirements</span></span>



| <span data-ttu-id="88726-112">Требование</span><span class="sxs-lookup"><span data-stu-id="88726-112">Requirement</span></span> | <span data-ttu-id="88726-113">Значение</span><span class="sxs-lookup"><span data-stu-id="88726-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88726-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88726-114">Minimum supported client</span></span><br/> | <span data-ttu-id="88726-115">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="88726-115">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="88726-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88726-116">Minimum supported server</span></span><br/> | <span data-ttu-id="88726-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="88726-117">None supported</span></span><br/>                                                          |
| <span data-ttu-id="88726-118">Header</span><span class="sxs-lookup"><span data-stu-id="88726-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="88726-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="88726-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
