---
description: Указывает, отправляет ли сетевой источник запросы на повторную отправку UDP в ответ на потерянные пакеты.
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: Свойство MFNETSOURCE_RESENDSENABLED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656563"
---
# <a name="mfnetsource_resendsenabled-property"></a><span data-ttu-id="51930-103">МФНЕТСАУРЦЕ \_ ресендсенаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="51930-103">MFNETSOURCE\_RESENDSENABLED property</span></span>

<span data-ttu-id="51930-104">Указывает, отправляет ли сетевой источник запросы на повторную отправку UDP в ответ на потерянные пакеты.</span><span class="sxs-lookup"><span data-stu-id="51930-104">Specifies whether the network source sends UDP resend requests in response to lost packets.</span></span>



<span data-ttu-id="51930-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="51930-105">Data type</span></span>

<span data-ttu-id="51930-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="51930-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="51930-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="51930-107">PROPVARIANT member</span></span>

<span data-ttu-id="51930-108">Логическое значение (**Long**)</span><span class="sxs-lookup"><span data-stu-id="51930-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="51930-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="51930-109">VT\_I4</span></span>

<span data-ttu-id="51930-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="51930-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="51930-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51930-111">Remarks</span></span>

<span data-ttu-id="51930-112">Константа **мфнетсаурце \_ ресендсенаблед** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="51930-112">The constant **MFNETSOURCE\_RESENDSENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="51930-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="51930-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="51930-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="51930-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="51930-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="51930-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="51930-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="51930-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="51930-117">Значение этого свойства по умолчанию равно **true**.</span><span class="sxs-lookup"><span data-stu-id="51930-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="51930-118">Требования</span><span class="sxs-lookup"><span data-stu-id="51930-118">Requirements</span></span>



| <span data-ttu-id="51930-119">Требование</span><span class="sxs-lookup"><span data-stu-id="51930-119">Requirement</span></span> | <span data-ttu-id="51930-120">Значение</span><span class="sxs-lookup"><span data-stu-id="51930-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51930-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51930-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51930-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51930-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="51930-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51930-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51930-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51930-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="51930-125">Header</span><span class="sxs-lookup"><span data-stu-id="51930-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="51930-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="51930-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51930-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51930-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51930-128">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="51930-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="51930-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51930-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="51930-130">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51930-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




