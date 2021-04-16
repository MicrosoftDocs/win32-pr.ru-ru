---
description: Заставляет Расширенный модуль подготовки видео (Евр) выполнять пакетный вызов метода IDirect3D9Device::P повторной отправки.
ms.assetid: d7523000-baa0-4011-97e1-d1ffe7263d01
title: Атрибут EVRConfig_ForceBatching (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6dff5d7a5e90377c8749519033b6a66ef7663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539542"
---
# <a name="evrconfig_forcebatching-attribute"></a><span data-ttu-id="072aa-103">Еврконфиг \_ форцебатчинг, атрибут</span><span class="sxs-lookup"><span data-stu-id="072aa-103">EVRConfig\_ForceBatching attribute</span></span>

<span data-ttu-id="072aa-104">Заставляет Расширенный модуль подготовки видео (Евр) выполнять пакетный вызов метода [**IDirect3D9Device::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) повторной отправки.</span><span class="sxs-lookup"><span data-stu-id="072aa-104">Forces the Enhanced Video Renderer (EVR) to batch calls to the [**IDirect3D9Device::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="072aa-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="072aa-105">Data type</span></span>

<span data-ttu-id="072aa-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="072aa-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="072aa-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="072aa-107">Get/set</span></span>

<span data-ttu-id="072aa-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="072aa-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="072aa-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="072aa-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="072aa-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="072aa-110">Remarks</span></span>

<span data-ttu-id="072aa-111">Этот атрибут можно задать в приемнике носителей Евр.</span><span class="sxs-lookup"><span data-stu-id="072aa-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="072aa-112">Чтобы задать атрибут, используйте **QueryInterface** , чтобы запросить приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="072aa-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="072aa-113">Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеорендерпрефс \_ ФОРЦЕБАТЧИНГ** в Евр.</span><span class="sxs-lookup"><span data-stu-id="072aa-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_ForceBatching** flag on the EVR.</span></span> <span data-ttu-id="072aa-114">Описание этого флага см. в разделе [**мфвидеорендерпрефс**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="072aa-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="072aa-115">Константа GUID для этого атрибута экспортируется из стрмиидс. lib.</span><span class="sxs-lookup"><span data-stu-id="072aa-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="072aa-116">Требования</span><span class="sxs-lookup"><span data-stu-id="072aa-116">Requirements</span></span>



| <span data-ttu-id="072aa-117">Требование</span><span class="sxs-lookup"><span data-stu-id="072aa-117">Requirement</span></span> | <span data-ttu-id="072aa-118">Значение</span><span class="sxs-lookup"><span data-stu-id="072aa-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="072aa-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="072aa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="072aa-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="072aa-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="072aa-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="072aa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="072aa-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="072aa-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="072aa-123">Header</span><span class="sxs-lookup"><span data-stu-id="072aa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="072aa-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="072aa-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="072aa-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="072aa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="072aa-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="072aa-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="072aa-127">Атрибуты Евр</span><span class="sxs-lookup"><span data-stu-id="072aa-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="072aa-128">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="072aa-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 
