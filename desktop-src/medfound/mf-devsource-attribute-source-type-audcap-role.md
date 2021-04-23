---
description: Указывает роль устройства для устройства записи звука.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080488"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a><span data-ttu-id="715db-103">\_ \_ \_ \_ \_ Атрибут роли АУДКАП для типа источника \_ атрибута MF девсаурце</span><span class="sxs-lookup"><span data-stu-id="715db-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ROLE attribute</span></span>

<span data-ttu-id="715db-104">Указывает роль устройства для устройства записи звука.</span><span class="sxs-lookup"><span data-stu-id="715db-104">Specifies the device role for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="715db-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="715db-105">Data type</span></span>

<span data-ttu-id="715db-106">**Ероле** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="715db-106">**ERole** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="715db-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="715db-107">Get/set</span></span>

<span data-ttu-id="715db-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="715db-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="715db-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="715db-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="715db-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="715db-110">Remarks</span></span>

<span data-ttu-id="715db-111">Тип перечисления **ероле** описан в основной документации по API аудио.</span><span class="sxs-lookup"><span data-stu-id="715db-111">The **eRole** enumeration type is documented in the Core Audio API documentation.</span></span>

<span data-ttu-id="715db-112">Значение атрибута указывает роль устройства.</span><span class="sxs-lookup"><span data-stu-id="715db-112">The value of the attribute specifies a device role.</span></span> <span data-ttu-id="715db-113">Этот атрибут используется со следующими функциями.</span><span class="sxs-lookup"><span data-stu-id="715db-113">This attribute is used with the following functions.</span></span>

<span data-ttu-id="715db-114">Этот атрибут может использоваться в качестве входных данных для функций [**мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) и [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="715db-114">This attribute can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="715db-115">Если атрибут указан, функция создает источник мультимедиа, использующий устройство записи звука по умолчанию для указанной роли устройства.</span><span class="sxs-lookup"><span data-stu-id="715db-115">If the attribute is specified, the function creates a media source that uses the default audio capture device for the specified device role.</span></span>

<span data-ttu-id="715db-116">Этот атрибут можно также использовать в качестве входных данных для функции [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="715db-116">This attribute can also be used as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="715db-117">Если атрибут указан, перечисление ограничивается указанной ролью устройства.</span><span class="sxs-lookup"><span data-stu-id="715db-117">If the attribute is specified, the enumeration is restricted to the specified device role.</span></span> <span data-ttu-id="715db-118">Кроме того, каждый объект активации, возвращаемый функцией **мфенумдевицесаурцес** , содержит этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="715db-118">In addition, each activation object returned by the **MFEnumDeviceSources** function contains this attribute.</span></span> <span data-ttu-id="715db-119">Атрибут затем используется объектом активации для внутренних целей при создании источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="715db-119">The attribute is then used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="715db-120">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="715db-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="715db-121">Требования</span><span class="sxs-lookup"><span data-stu-id="715db-121">Requirements</span></span>



| <span data-ttu-id="715db-122">Требование</span><span class="sxs-lookup"><span data-stu-id="715db-122">Requirement</span></span> | <span data-ttu-id="715db-123">Значение</span><span class="sxs-lookup"><span data-stu-id="715db-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="715db-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="715db-124">Minimum supported client</span></span><br/> | <span data-ttu-id="715db-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="715db-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="715db-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="715db-126">Minimum supported server</span></span><br/> | <span data-ttu-id="715db-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="715db-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="715db-128">Header</span><span class="sxs-lookup"><span data-stu-id="715db-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="715db-129"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="715db-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="715db-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="715db-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="715db-131">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="715db-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="715db-132">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="715db-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="715db-133">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="715db-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




