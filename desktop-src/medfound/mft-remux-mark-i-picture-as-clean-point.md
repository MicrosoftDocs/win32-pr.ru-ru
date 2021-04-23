---
description: Указывает, следует ли помечать файловую таблицу H. 264 Video ремукс как чистую точку для улучшения возможностей поиска. Это может привести к повреждениям при поиске в несоответствующих окончательных MP4-файлах.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: Атрибут MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702032"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a><span data-ttu-id="bb6ca-104">MFT \_ ремукс \_ отметить \_ \_ \_ как \_ \_ атрибут пустой точки</span><span class="sxs-lookup"><span data-stu-id="bb6ca-104">MFT\_REMUX\_MARK\_I\_PICTURE\_AS\_CLEAN\_POINT attribute</span></span>

<span data-ttu-id="bb6ca-105">Указывает, следует ли помечать файловую таблицу H. 264 Video ремукс как чистую точку для улучшения возможностей поиска.</span><span class="sxs-lookup"><span data-stu-id="bb6ca-105">Specifies whether the H.264 video remux MFT should mark I pictures as clean point for better seek-ability.</span></span> <span data-ttu-id="bb6ca-106">Это может привести к повреждениям при поиске в несоответствующих окончательных MP4-файлах.</span><span class="sxs-lookup"><span data-stu-id="bb6ca-106">This has the potential for corruptions on seeks in non-conforming final MP4 files.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb6ca-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bb6ca-107">Data type</span></span>

<span data-ttu-id="bb6ca-108">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="bb6ca-108">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bb6ca-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb6ca-109">Remarks</span></span>

<span data-ttu-id="bb6ca-110">Изображение с очисткой точек должно быть сжато IDR изображения по определению.</span><span class="sxs-lookup"><span data-stu-id="bb6ca-110">Clean point picture should be compressed IDR pictures by definition.</span></span>

<span data-ttu-id="bb6ca-111">Это не рекомендуется для записи или ремуксинг файлов MP4, если это не требуется для создания некоторых промежуточных файлов псевдо-MP4 для редактирования видео.</span><span class="sxs-lookup"><span data-stu-id="bb6ca-111">This is not recommended for recording or remuxing MP4 files, unless such an exercise is to produce some intermediate pseudo MP4 files for video editing.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6ca-112">Требования</span><span class="sxs-lookup"><span data-stu-id="bb6ca-112">Requirements</span></span>



| <span data-ttu-id="bb6ca-113">Требование</span><span class="sxs-lookup"><span data-stu-id="bb6ca-113">Requirement</span></span> | <span data-ttu-id="bb6ca-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bb6ca-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6ca-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb6ca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6ca-116">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="bb6ca-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="bb6ca-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb6ca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6ca-118">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="bb6ca-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="bb6ca-119">Header</span><span class="sxs-lookup"><span data-stu-id="bb6ca-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb6ca-120"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ca-120"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb6ca-121">IDL</span><span class="sxs-lookup"><span data-stu-id="bb6ca-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb6ca-122"><dt>Мфтрансформ. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ca-122"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb6ca-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb6ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6ca-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb6ca-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




