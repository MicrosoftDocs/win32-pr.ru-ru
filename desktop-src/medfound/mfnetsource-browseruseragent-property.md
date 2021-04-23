---
description: Значение первой части \# поля &0034; CS (User-Agent) &\# 0034;, используемое сетевым источником для ведения журнала.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: Свойство MFNETSOURCE_BROWSERUSERAGENT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cbb4dcd5558c59da20e75209529c16fc0c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543207"
---
# <a name="mfnetsource_browseruseragent-property"></a><span data-ttu-id="bc3bb-103">МФНЕТСАУРЦЕ \_ бровсерусеражент, свойство</span><span class="sxs-lookup"><span data-stu-id="bc3bb-103">MFNETSOURCE\_BROWSERUSERAGENT property</span></span>

<span data-ttu-id="bc3bb-104">Значение первой части поля "CS (User-Agent)", используемое сетевым источником для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="bc3bb-104">The value of the first portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="bc3bb-105">Приложения могут задать для этого свойства любое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="bc3bb-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="bc3bb-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bc3bb-106">Data type</span></span>

<span data-ttu-id="bc3bb-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="bc3bb-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bc3bb-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="bc3bb-108">PROPVARIANT member</span></span>

<span data-ttu-id="bc3bb-109">Строка расширенных символов (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="bc3bb-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="bc3bb-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="bc3bb-110">VT\_LPWSTR</span></span>

<span data-ttu-id="bc3bb-111">**пвсзвал**</span><span class="sxs-lookup"><span data-stu-id="bc3bb-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bc3bb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc3bb-112">Remarks</span></span>

<span data-ttu-id="bc3bb-113">Константа **мфнетсаурце \_ бровсерусеражент** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="bc3bb-113">The constant **MFNETSOURCE\_BROWSERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="bc3bb-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="bc3bb-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="bc3bb-115">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="bc3bb-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="bc3bb-116">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="bc3bb-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="bc3bb-117">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="bc3bb-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc3bb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bc3bb-118">Requirements</span></span>



| <span data-ttu-id="bc3bb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bc3bb-119">Requirement</span></span> | <span data-ttu-id="bc3bb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bc3bb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3bb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc3bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3bb-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc3bb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bc3bb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc3bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3bb-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc3bb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bc3bb-125">Header</span><span class="sxs-lookup"><span data-stu-id="bc3bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc3bb-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc3bb-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc3bb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc3bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3bb-128">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="bc3bb-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="bc3bb-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bc3bb-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bc3bb-130">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bc3bb-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bc3bb-131">**МФНЕТСАУРЦЕ \_ плайерусеражент**</span><span class="sxs-lookup"><span data-stu-id="bc3bb-131">**MFNETSOURCE\_PLAYERUSERAGENT**</span></span>](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




