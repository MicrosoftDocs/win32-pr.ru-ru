---
description: Отключает использование подключаемых модулей камеры, выполняемых после обработки, модулем чтения исходного кода.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: Атрибут MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272380"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a><span data-ttu-id="db2c1-103">\_Чтение источника \_ MF \_ Отключить \_ \_ атрибут подключаемых модулей камеры</span><span class="sxs-lookup"><span data-stu-id="db2c1-103">MF\_SOURCE\_READER\_DISABLE\_CAMERA\_PLUGINS attribute</span></span>

<span data-ttu-id="db2c1-104">Отключает использование подключаемых модулей камеры, выполняемых после обработки, модулем [чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="db2c1-104">Disables the use of post-processing camera plug-ins by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="db2c1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="db2c1-105">Data type</span></span>

<span data-ttu-id="db2c1-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="db2c1-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="db2c1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db2c1-107">Remarks</span></span>

<span data-ttu-id="db2c1-108">Этот атрибут применяется, когда модуль чтения исходного кода используется с источником видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="db2c1-108">This attribute applies when the Source Reader is used with a video capture source.</span></span> <span data-ttu-id="db2c1-109">Если этот атрибут имеет **значение true**, то модуль чтения исходного кода не сможет загружать какие-либо подключаемые модули последующей обработки, которые может предоставить камера.</span><span class="sxs-lookup"><span data-stu-id="db2c1-109">If this attribute is **TRUE**, it prevents the Source Reader from loading any post-processing plug-ins that the camera might provide.</span></span> <span data-ttu-id="db2c1-110">В противном случае по умолчанию средство чтения источника загрузит их.</span><span class="sxs-lookup"><span data-stu-id="db2c1-110">Otherwise, by default the Source Reader will load them.</span></span>

<span data-ttu-id="db2c1-111">Значение этого атрибута по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="db2c1-111">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="db2c1-112">Задайте атрибут при создании модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="db2c1-112">Set the attribute when you create the source reader.</span></span>

## <a name="requirements"></a><span data-ttu-id="db2c1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="db2c1-113">Requirements</span></span>



| <span data-ttu-id="db2c1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="db2c1-114">Requirement</span></span> | <span data-ttu-id="db2c1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="db2c1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db2c1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db2c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db2c1-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="db2c1-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="db2c1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db2c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db2c1-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="db2c1-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="db2c1-120">Header</span><span class="sxs-lookup"><span data-stu-id="db2c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="db2c1-121"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="db2c1-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db2c1-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db2c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db2c1-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db2c1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="db2c1-124">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="db2c1-124">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




