---
description: Указывает, включены ли все протоколы загрузки.
ms.assetid: c178693f-44ea-481e-b7f2-2ec94eea1994
title: Свойство MFNETSOURCE_ENABLE_DOWNLOAD (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1b57d8ab984f7c198d1c1b43455f2d0d5dda68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080379"
---
# <a name="mfnetsource_enable_download-property"></a><span data-ttu-id="c4cc6-103">МФНЕТСАУРЦЕ \_ включить \_ свойство скачивания</span><span class="sxs-lookup"><span data-stu-id="c4cc6-103">MFNETSOURCE\_ENABLE\_DOWNLOAD property</span></span>

<span data-ttu-id="c4cc6-104">Указывает, включены ли все протоколы загрузки.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-104">Specifies whether all download protocols are enabled.</span></span>



<span data-ttu-id="c4cc6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c4cc6-105">Data type</span></span>

<span data-ttu-id="c4cc6-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="c4cc6-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c4cc6-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="c4cc6-107">PROPVARIANT member</span></span>

<span data-ttu-id="c4cc6-108">Логическое значение (**Long**)</span><span class="sxs-lookup"><span data-stu-id="c4cc6-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="c4cc6-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c4cc6-109">VT\_I4</span></span>

<span data-ttu-id="c4cc6-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c4cc6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4cc6-111">Remarks</span></span>

<span data-ttu-id="c4cc6-112">При **\_ \_ загрузке Constant мфнетсаурце Enable** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-112">The constant **MFNETSOURCE\_ENABLE\_DOWNLOAD** defines the GUID for this property key.</span></span> <span data-ttu-id="c4cc6-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="c4cc6-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="c4cc6-115">Чтобы задать свойство, передайте **ипропертисторе** указатель на [конфигурацию источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c4cc6-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4cc6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c4cc6-116">Requirements</span></span>



| <span data-ttu-id="c4cc6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c4cc6-117">Requirement</span></span> | <span data-ttu-id="c4cc6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c4cc6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4cc6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4cc6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4cc6-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4cc6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c4cc6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4cc6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4cc6-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4cc6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c4cc6-123">Header</span><span class="sxs-lookup"><span data-stu-id="c4cc6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4cc6-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4cc6-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4cc6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4cc6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4cc6-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c4cc6-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c4cc6-127">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c4cc6-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="c4cc6-128">Поддерживаемые протоколы</span><span class="sxs-lookup"><span data-stu-id="c4cc6-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




