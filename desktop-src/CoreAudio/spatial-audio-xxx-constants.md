---
description: '\_ \_ Константы пространственного аудио XXX определяют значения, связанные с функциями пространственного звука.'
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Константы SPATIAL_AUDIO_XXX (Спатиалаудиометадата. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648935"
---
# <a name="spatial_audio_xxx-constants"></a><span data-ttu-id="796c9-103">\_ \_ Константы пространственного аудио XXX</span><span class="sxs-lookup"><span data-stu-id="796c9-103">SPATIAL\_AUDIO\_XXX Constants</span></span>

<span data-ttu-id="796c9-104">\_ \_ Константы пространственного аудио XXX определяют значения, связанные с функциями пространственного звука.</span><span class="sxs-lookup"><span data-stu-id="796c9-104">The SPATIAL\_AUDIO\_XXX constants define values related to spatial sound features.</span></span>



| <span data-ttu-id="796c9-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="796c9-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="796c9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="796c9-106">Description</span></span>                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <span data-ttu-id="796c9-107"><dt>**Пространственный \_ \_Расположение аудио**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="796c9-107"><dt>**SPATIAL\_AUDIO\_POSITION**</dt> <dt>200</dt></span></span> </dl>                                                   | <span data-ttu-id="796c9-108">Стандартная определяемая корпорацией Майкрософт команда пространственных метаданных, которая представляет позицию прослушивателя в стандартной модели, используемой [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , где заголовок прослушивателя находится в координатах (0, 0, 0), определенном в метрах.</span><span class="sxs-lookup"><span data-stu-id="796c9-108">A standard Microsoft-defined spatial audio metadata command which represents the listener position in the standard model used by [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) where the listener's head is position at coordinates (0,0,0), defined in meters.</span></span><br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <span data-ttu-id="796c9-109"><dt>**Пространственный \_ \_ \_ \_ Число байтов в байтах для позиций**</dt> <dt>(float) \* 3</dt></span><span class="sxs-lookup"><span data-stu-id="796c9-109"><dt>**SPATIAL\_AUDIO\_POSITION\_BYTE\_COUNT**</dt> <dt>sizeof(float) \* 3</dt></span></span> </dl> | <span data-ttu-id="796c9-110">Указывает размер значения **пространственного расположения для \_ звука \_** .</span><span class="sxs-lookup"><span data-stu-id="796c9-110">Specifies the size of the **SPATIAL\_AUDIO\_POSITION** value.</span></span><br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <span data-ttu-id="796c9-111"><dt>**Пространственный \_ \_Стандартные \_ команды AUDIO \_ Start**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="796c9-111"><dt>**SPATIAL\_AUDIO\_STANDARD\_COMMANDS\_START**</dt> <dt>200</dt></span></span> </dl>    | <span data-ttu-id="796c9-112">Указывает начало диапазона команд зарезервированных пространственных метаданных (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="796c9-112">Specifies the start of the range of Microsoft-reserved spatial audio metadata commands.</span></span> <span data-ttu-id="796c9-113">Команды пользовательских метаданных ограничены идентификаторами команд 0-199.</span><span class="sxs-lookup"><span data-stu-id="796c9-113">Custom metadata commands are restricted to command IDs 0 - 199.</span></span> <span data-ttu-id="796c9-114">Команды 200-255 зарезервированы для использования корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="796c9-114">Commands 200 - 255 are reserved for Microsoft use.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="796c9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="796c9-115">Requirements</span></span>



| <span data-ttu-id="796c9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="796c9-116">Requirement</span></span> | <span data-ttu-id="796c9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="796c9-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="796c9-118">Header</span><span class="sxs-lookup"><span data-stu-id="796c9-118">Header</span></span><br/> | <dl> <span data-ttu-id="796c9-119"><dt>Спатиалаудиометадата. h</dt></span><span class="sxs-lookup"><span data-stu-id="796c9-119"><dt>SpatialAudioMetadata.h</dt></span></span> </dl> |



 

 




