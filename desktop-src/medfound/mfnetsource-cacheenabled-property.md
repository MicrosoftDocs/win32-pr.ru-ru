---
description: Указывает, кэширует ли сетевой источник содержимое.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: Свойство MFNETSOURCE_CACHEENABLED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6f38398e44eaa25da7a5b1f88a76edb8e40924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897930"
---
# <a name="mfnetsource_cacheenabled-property"></a><span data-ttu-id="08605-103">МФНЕТСАУРЦЕ \_ качинаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="08605-103">MFNETSOURCE\_CACHEENABLED property</span></span>

<span data-ttu-id="08605-104">Указывает, кэширует ли сетевой источник содержимое.</span><span class="sxs-lookup"><span data-stu-id="08605-104">Specifies whether the network source caches content.</span></span>



<span data-ttu-id="08605-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="08605-105">Data type</span></span>

<span data-ttu-id="08605-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="08605-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="08605-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="08605-107">PROPVARIANT member</span></span>

<span data-ttu-id="08605-108">Логическое значение (**Long**)</span><span class="sxs-lookup"><span data-stu-id="08605-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="08605-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="08605-109">VT\_I4</span></span>

<span data-ttu-id="08605-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="08605-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="08605-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08605-111">Remarks</span></span>

<span data-ttu-id="08605-112">Константа **мфнетсаурце \_ качинаблед** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="08605-112">The constant **MFNETSOURCE\_CACHEENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="08605-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="08605-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="08605-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="08605-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="08605-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="08605-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="08605-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="08605-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="08605-117">Значение этого свойства по умолчанию равно **true**.</span><span class="sxs-lookup"><span data-stu-id="08605-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="08605-118">Требования</span><span class="sxs-lookup"><span data-stu-id="08605-118">Requirements</span></span>



| <span data-ttu-id="08605-119">Требование</span><span class="sxs-lookup"><span data-stu-id="08605-119">Requirement</span></span> | <span data-ttu-id="08605-120">Значение</span><span class="sxs-lookup"><span data-stu-id="08605-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08605-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08605-121">Minimum supported client</span></span><br/> | <span data-ttu-id="08605-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08605-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="08605-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08605-123">Minimum supported server</span></span><br/> | <span data-ttu-id="08605-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08605-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="08605-125">Header</span><span class="sxs-lookup"><span data-stu-id="08605-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="08605-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="08605-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08605-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08605-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08605-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08605-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="08605-129">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08605-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




