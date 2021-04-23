---
description: Указывает, включает ли модуль чтения исходного экрана ускорение видео DirectX (ДКСВА) для видеодекодера.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: Атрибут MF_SOURCE_READER_DISABLE_DXVA (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348735"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a><span data-ttu-id="1c6ad-103">\_Чтение источника \_ MF \_ Отключить \_ атрибут дксва</span><span class="sxs-lookup"><span data-stu-id="1c6ad-103">MF\_SOURCE\_READER\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="1c6ad-104">Указывает, включает ли [модуль чтения исходного](source-reader.md) экрана ускорение видео DirectX (дксва) для видеодекодера.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-104">Specifies whether the [Source Reader](source-reader.md) enables DirectX Video Acceleration (DXVA) on the video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c6ad-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1c6ad-105">Data type</span></span>

<span data-ttu-id="1c6ad-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1c6ad-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="1c6ad-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="1c6ad-107">Get/set</span></span>

<span data-ttu-id="1c6ad-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1c6ad-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1c6ad-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="1c6ad-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c6ad-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c6ad-110">Remarks</span></span>

<span data-ttu-id="1c6ad-111">Этот атрибут применяется, если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-111">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="1c6ad-112">Модуль чтения исходного кода декодирует поток видео.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-112">The source reader decodes a video stream.</span></span>
-   <span data-ttu-id="1c6ad-113">Видеодекодер поддерживает декодирование ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-113">The video decoder supports DXVA decoding.</span></span>
-   <span data-ttu-id="1c6ad-114">Приложение использует атрибут [ \_ \_ \_ \_ диспетчера D3D источника MF](mf-source-reader-d3d-manager.md) для установки [Диспетчер устройств Direct3D](direct3d-device-manager.md) в модуле чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-114">The application uses the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute to set the [Direct3D Device Manager](direct3d-device-manager.md) on the source reader.</span></span>

<span data-ttu-id="1c6ad-115">Этот атрибут позволяет приложению отключить ДКСВА, продолжая декодироваться на поверхности Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-115">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="1c6ad-116">По умолчанию модуль чтения исходного кода использует [Диспетчер устройств Direct3D](direct3d-device-manager.md) в двух целях:</span><span class="sxs-lookup"><span data-stu-id="1c6ad-116">By default, the source reader uses the [Direct3D Device Manager](direct3d-device-manager.md) for two purposes:</span></span>

-   <span data-ttu-id="1c6ad-117">Включение декодирования ДКСВА в видеодекодере.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-117">To enable DXVA decoding in the video decoder.</span></span>
-   <span data-ttu-id="1c6ad-118">Для выделения поверхностей Direct3D для видеороликов.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-118">To allocate Direct3D surfaces for the video samples.</span></span>

<span data-ttu-id="1c6ad-119">Если значение \_ \_ атрибута дксва чтения источника MF \_ \_ равно **true**, модуль чтения исходного кода отключает декодирование дксва, хотя он по-прежнему использует [Диспетчер устройств Direct3D](direct3d-device-manager.md) для выделения поверхностей Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-119">If the value of the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is **TRUE**, the source reader does disables DXVA decoding, although it still uses the [Direct3D Device Manager](direct3d-device-manager.md) to allocate Direct3D surfaces.</span></span>

<span data-ttu-id="1c6ad-120">Если атрибут [ \_ \_ \_ \_ диспетчера D3D источника данных MF](mf-source-reader-d3d-manager.md) не ЗАДАН, то \_ модуль чтения источника MF \_ \_ disable \_ дксва не учитывается.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-120">If the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute is not set, the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is ignored.</span></span>

<span data-ttu-id="1c6ad-121">Значение этого атрибута по умолчанию равно **false**, означающее, что при наличии включен декодирование дксва.</span><span class="sxs-lookup"><span data-stu-id="1c6ad-121">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6ad-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1c6ad-122">Requirements</span></span>



| <span data-ttu-id="1c6ad-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1c6ad-123">Requirement</span></span> | <span data-ttu-id="1c6ad-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1c6ad-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6ad-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c6ad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6ad-126">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="1c6ad-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="1c6ad-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c6ad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6ad-128">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="1c6ad-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1c6ad-129">Header</span><span class="sxs-lookup"><span data-stu-id="1c6ad-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c6ad-130"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c6ad-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c6ad-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c6ad-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6ad-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c6ad-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c6ad-133">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="1c6ad-133">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="1c6ad-134">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="1c6ad-134">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




