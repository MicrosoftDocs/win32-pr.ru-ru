---
description: Указывает, включено ли переключение потоков в источнике сети.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: Свойство MFNETSOURCE_THINNINGENABLED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990834"
---
# <a name="mfnetsource_thinningenabled-property"></a><span data-ttu-id="a97c4-103">МФНЕТСАУРЦЕ \_ синнинженаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="a97c4-103">MFNETSOURCE\_THINNINGENABLED property</span></span>

<span data-ttu-id="a97c4-104">Указывает, включено ли переключение потоков в источнике сети.</span><span class="sxs-lookup"><span data-stu-id="a97c4-104">Specifies whether stream switching is enabled on the network source.</span></span> <span data-ttu-id="a97c4-105">Переключение потоков позволяет серверу мультимедиа изменять потоки в файле с несколькими скоростями (MBR) в зависимости от доступной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="a97c4-105">Stream switching enables the media server to change streams in a multiple bit-rate (MBR) file, based on available bandwidth.</span></span>



<span data-ttu-id="a97c4-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a97c4-106">Data type</span></span>

<span data-ttu-id="a97c4-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="a97c4-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a97c4-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="a97c4-108">PROPVARIANT member</span></span>

<span data-ttu-id="a97c4-109">Логическое значение (**Long**)</span><span class="sxs-lookup"><span data-stu-id="a97c4-109">Boolean (**LONG**)</span></span>

<span data-ttu-id="a97c4-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a97c4-110">VT\_I4</span></span>

<span data-ttu-id="a97c4-111">**лвал**</span><span class="sxs-lookup"><span data-stu-id="a97c4-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a97c4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a97c4-112">Remarks</span></span>

<span data-ttu-id="a97c4-113">Константа **мфнетсаурце \_ синнинженаблед** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="a97c4-113">The constant **MFNETSOURCE\_THINNINGENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="a97c4-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a97c4-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a97c4-115">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="a97c4-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a97c4-116">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="a97c4-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a97c4-117">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a97c4-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="a97c4-118">Значение этого свойства по умолчанию равно **true**.</span><span class="sxs-lookup"><span data-stu-id="a97c4-118">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a97c4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a97c4-119">Requirements</span></span>



| <span data-ttu-id="a97c4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a97c4-120">Requirement</span></span> | <span data-ttu-id="a97c4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a97c4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a97c4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a97c4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a97c4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a97c4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a97c4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a97c4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a97c4-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a97c4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a97c4-126">Header</span><span class="sxs-lookup"><span data-stu-id="a97c4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a97c4-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a97c4-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a97c4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a97c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a97c4-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a97c4-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a97c4-130">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a97c4-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




