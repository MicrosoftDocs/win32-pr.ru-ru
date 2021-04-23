---
description: Задает поворот видеокадра в направлении против часовой стрелки.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: Атрибут MF_MT_VIDEO_ROTATION (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913555"
---
# <a name="mf_mt_video_rotation-attribute"></a><span data-ttu-id="7831f-103">\_ \_ Атрибут поворота видео MF MT \_</span><span class="sxs-lookup"><span data-stu-id="7831f-103">MF\_MT\_VIDEO\_ROTATION attribute</span></span>

<span data-ttu-id="7831f-104">Задает поворот видеокадра в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="7831f-104">Specifies the rotation of a video frame in the counter-clockwise direction.</span></span>

## <a name="data-type"></a><span data-ttu-id="7831f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7831f-105">Data type</span></span>

<span data-ttu-id="7831f-106">**Мфвидеоротатионформат** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7831f-106">**MFVideoRotationFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7831f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7831f-107">Remarks</span></span>

<span data-ttu-id="7831f-108">Видео с карманного устройства, например мобильного телефона, часто поворачивается на 90, 180 или 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="7831f-108">Video from a handheld device, such as a mobile phone, is often rotated by 90, 180, or 270 degrees.</span></span> <span data-ttu-id="7831f-109">Если камера сохраняет ориентацию в виде метаданных в видеофайл, образ можно настроить во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7831f-109">If the camera stores the orientation as metadata in the video file, the image can be adjusted at the time of playback.</span></span>

<span data-ttu-id="7831f-110">Если этому атрибуту присвоено значение **мфвидеоротатионформат \_ 90**, это означает, что содержимое повернуто на 90 градусов в направлении по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="7831f-110">If this attribute set to **MFVideoRotationFormat\_90**, it means that the content has been rotated 90 degrees in the counter-clockwise direction.</span></span> <span data-ttu-id="7831f-111">Если содержимое было повернуто на 90 градусов по часовой стрелке, значение атрибута будет равно **мфвидеоротатионформат \_ 270**.</span><span class="sxs-lookup"><span data-stu-id="7831f-111">If the content was rotated 90 degrees in the clockwise direction, the attribute value would be **MFVideoRotationFormat\_270**.</span></span>

<span data-ttu-id="7831f-112">Поддерживаемые значения для этого атрибута перечислены в [**мфвидеоротатионформат**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span><span class="sxs-lookup"><span data-stu-id="7831f-112">The supported values for this attribute are enumerated in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span></span>

<span data-ttu-id="7831f-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="7831f-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7831f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7831f-114">Requirements</span></span>



| <span data-ttu-id="7831f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7831f-115">Requirement</span></span> | <span data-ttu-id="7831f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7831f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7831f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7831f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7831f-118">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="7831f-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7831f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7831f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7831f-120">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="7831f-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7831f-121">Header</span><span class="sxs-lookup"><span data-stu-id="7831f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7831f-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7831f-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7831f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7831f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7831f-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7831f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7831f-125">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="7831f-125">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




