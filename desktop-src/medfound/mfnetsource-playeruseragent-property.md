---
description: Значение второй части &\# 0034; CS (User-Agent) &\# 0034;, используемое сетевым источником для ведения журнала.
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: Свойство MFNETSOURCE_PLAYERUSERAGENT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f4d06eaea566e22e1239ed04594f2f592c7cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719360"
---
# <a name="mfnetsource_playeruseragent-property"></a><span data-ttu-id="2b29d-103">МФНЕТСАУРЦЕ \_ плайерусеражент, свойство</span><span class="sxs-lookup"><span data-stu-id="2b29d-103">MFNETSOURCE\_PLAYERUSERAGENT property</span></span>

<span data-ttu-id="2b29d-104">Значение второй части поля "CS (User-Agent)", используемое сетевым источником для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="2b29d-104">The value of the second portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="2b29d-105">Приложения могут задать для этого свойства любое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="2b29d-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="2b29d-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2b29d-106">Data type</span></span>

<span data-ttu-id="2b29d-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="2b29d-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2b29d-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="2b29d-108">PROPVARIANT member</span></span>

<span data-ttu-id="2b29d-109">Строка расширенных символов (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="2b29d-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="2b29d-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="2b29d-110">VT\_LPWSTR</span></span>

<span data-ttu-id="2b29d-111">**пвсзвал**</span><span class="sxs-lookup"><span data-stu-id="2b29d-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2b29d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b29d-112">Remarks</span></span>

<span data-ttu-id="2b29d-113">Константа **мфнетсаурце \_ плайерусеражент** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="2b29d-113">The constant **MFNETSOURCE\_PLAYERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="2b29d-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2b29d-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="2b29d-115">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="2b29d-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="2b29d-116">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="2b29d-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="2b29d-117">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2b29d-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b29d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2b29d-118">Requirements</span></span>



| <span data-ttu-id="2b29d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2b29d-119">Requirement</span></span> | <span data-ttu-id="2b29d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2b29d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b29d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b29d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b29d-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b29d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2b29d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b29d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b29d-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b29d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2b29d-125">Header</span><span class="sxs-lookup"><span data-stu-id="2b29d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b29d-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b29d-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b29d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b29d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b29d-128">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="2b29d-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="2b29d-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b29d-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2b29d-130">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b29d-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2b29d-131">**МФНЕТСАУРЦЕ \_ бровсерусеражент**</span><span class="sxs-lookup"><span data-stu-id="2b29d-131">**MFNETSOURCE\_BROWSERUSERAGENT**</span></span>](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




