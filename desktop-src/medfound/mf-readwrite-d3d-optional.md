---
description: Указывает, требует ли приложение поддержки Microsoft Direct3D в модуле чтения источника или в модуле записи приемника.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: Атрибут MF_READWRITE_D3D_OPTIONAL (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272503"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a><span data-ttu-id="adb52-103">\_ \_ \_ Необязательный атрибут D3D ReadWrite</span><span class="sxs-lookup"><span data-stu-id="adb52-103">MF\_READWRITE\_D3D\_OPTIONAL attribute</span></span>

<span data-ttu-id="adb52-104">Указывает, требует ли приложение поддержки Microsoft Direct3D в [модуле чтения источника](source-reader.md) или в [модуле записи приемника](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="adb52-104">Specifies whether the application requires Microsoft Direct3D support in the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="adb52-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="adb52-105">Data type</span></span>

<span data-ttu-id="adb52-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="adb52-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="adb52-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adb52-107">Remarks</span></span>

<span data-ttu-id="adb52-108">Этот атрибут применяется только в том случае, если приложение включает поддержку Direct3D с помощью атрибута [ \_ \_ \_ \_ диспетчера](mf-sink-writer-d3d-manager.md) D3D [ \_ \_ модуля чтения \_ \_ ](mf-source-reader-d3d-manager.md) журнала "MF" или MF.</span><span class="sxs-lookup"><span data-stu-id="adb52-108">This attribute applies only if the application enables Direct3D support using the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) or [MF\_SINK\_WRITER\_D3D\_MANAGER](mf-sink-writer-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="adb52-109">Если приложение включает поддержку Direct3D, модуль чтения исходного кода и модуль записи приемника пытаются выделить поверхности Direct3D для видео.</span><span class="sxs-lookup"><span data-stu-id="adb52-109">If the application enables Direct3D support, the Source Reader and Sink Writer will both try to allocate Direct3D surfaces for video.</span></span> <span data-ttu-id="adb52-110">Если это не удается, а \_ \_ \_ необязательный атрибут D3D на MF ReadWrite имеет **значение true**, то модуль чтения и приемника источника будет переключаться на выделение видеообластей в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="adb52-110">If this fails, and the MF\_READWRITE\_D3D\_OPTIONAL attribute is **TRUE**, the Source Reader/Sink Writer will fall back to allocating video surfaces in system memory.</span></span> <span data-ttu-id="adb52-111">В противном случае, если поверхности Direct3D не могут быть выделены и MF \_ ReadWrite \_ \_ (необязательно), **то** при обработке возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="adb52-111">Otherwise, if Direct3D surfaces cannot be allocated and MF\_READWRITE\_D3D\_OPTIONAL is **FALSE**, an error occurs during processing.</span></span>

<span data-ttu-id="adb52-112">Если приложение не поддерживает поддержку Direct3D, модуль чтения и приемник исходного кода использует память системы и не учитывает значение \_ \_ необязательной D3D-памяти MF ReadWrite \_ .</span><span class="sxs-lookup"><span data-stu-id="adb52-112">If the application does not enable Direct3D support, the Source Reader/Sink Writer uses system memory, and ignores the value of MF\_READWRITE\_D3D\_OPTIONAL.</span></span>

<span data-ttu-id="adb52-113">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="adb52-113">This attribute is optional.</span></span> <span data-ttu-id="adb52-114">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="adb52-114">The default value is **FALSE**.</span></span> <span data-ttu-id="adb52-115">Задайте атрибут при создании модуля чтения источника или средства записи приемника.</span><span class="sxs-lookup"><span data-stu-id="adb52-115">Set the attribute when you create the Source Reader or Sink Writer.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb52-116">Требования</span><span class="sxs-lookup"><span data-stu-id="adb52-116">Requirements</span></span>



| <span data-ttu-id="adb52-117">Требование</span><span class="sxs-lookup"><span data-stu-id="adb52-117">Requirement</span></span> | <span data-ttu-id="adb52-118">Значение</span><span class="sxs-lookup"><span data-stu-id="adb52-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="adb52-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adb52-119">Minimum supported client</span></span><br/> | <span data-ttu-id="adb52-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="adb52-120">Windows 8 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="adb52-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adb52-121">Minimum supported server</span></span><br/> | <span data-ttu-id="adb52-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="adb52-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="adb52-123">Header</span><span class="sxs-lookup"><span data-stu-id="adb52-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="adb52-124"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="adb52-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adb52-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adb52-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb52-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="adb52-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="adb52-127">Атрибуты модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="adb52-127">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="adb52-128">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="adb52-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




