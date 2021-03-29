---
description: Определяемый декодером идентификатор GUID, определяющий формат метаданных пространственного звука, уведомляющий нисходящие компоненты типа объекта метаданных, который будет выводить декодер.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: Атрибут MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264751"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a><span data-ttu-id="0a471-103">\_ \_ \_ \_ Идентификатор формата МЕТАДАННЫХ объекта пространственного звука MF MT \_ \_ \_ атрибут идентификатора</span><span class="sxs-lookup"><span data-stu-id="0a471-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_FORMAT\_ID attribute</span></span>

<span data-ttu-id="0a471-104">Определяемый декодером идентификатор GUID, определяющий формат метаданных пространственного звука, уведомляющий нисходящие компоненты типа объекта метаданных, который будет выводить декодер.</span><span class="sxs-lookup"><span data-stu-id="0a471-104">A decoder-defined GUID that identifies the spatial audio metadata format, notifying downstream components of the metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="0a471-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0a471-105">Data type</span></span>

<span data-ttu-id="0a471-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="0a471-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="0a471-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a471-107">Remarks</span></span>

<span data-ttu-id="0a471-108">Большой двоичный объект метаданных с указанным форматом записывается с помощью интерфейса [**испатиалаудиометадатавритер**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) и считывается с помощью интерфейса [**испатиалаудиометадатареадер**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="0a471-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="0a471-109">Большой двоичный объект метаданных непрозрачен для Media Foundation конвейера и компонентов.</span><span class="sxs-lookup"><span data-stu-id="0a471-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="0a471-110">Атрибут применяется к типу пространственного звукового носителя.</span><span class="sxs-lookup"><span data-stu-id="0a471-110">The attribute is applied to the spatial audio media type.</span></span> <span data-ttu-id="0a471-111">Если нисходящий компонент не поддерживает формат метаданных, заданный идентификатором GUID, компонент должен отклонять входной тип носителя.</span><span class="sxs-lookup"><span data-stu-id="0a471-111">If a downstream component does not support the metadata format specified by the GUID, the component should reject the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a471-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0a471-112">Requirements</span></span>



| <span data-ttu-id="0a471-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0a471-113">Requirement</span></span> | <span data-ttu-id="0a471-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0a471-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a471-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a471-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0a471-116">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="0a471-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0a471-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a471-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0a471-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0a471-118">None supported</span></span><br/>                                                          |
| <span data-ttu-id="0a471-119">Header</span><span class="sxs-lookup"><span data-stu-id="0a471-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a471-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a471-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
