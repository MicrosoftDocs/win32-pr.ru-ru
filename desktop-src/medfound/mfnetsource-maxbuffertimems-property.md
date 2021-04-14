---
description: Максимальный объем данных, допустимых для сетевых буферов источника (в миллисекундах).
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: Свойство MFNETSOURCE_MAXBUFFERTIMEMS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692504"
---
# <a name="mfnetsource_maxbuffertimems-property"></a><span data-ttu-id="177ed-103">МФНЕТСАУРЦЕ \_ максбуффертимемс, свойство</span><span class="sxs-lookup"><span data-stu-id="177ed-103">MFNETSOURCE\_MAXBUFFERTIMEMS property</span></span>

<span data-ttu-id="177ed-104">Максимальный объем данных, допустимых для сетевых буферов источника (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="177ed-104">Maximum amount of data the network source buffers, in milliseconds.</span></span>



<span data-ttu-id="177ed-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="177ed-105">Data type</span></span>

<span data-ttu-id="177ed-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="177ed-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="177ed-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="177ed-107">PROPVARIANT member</span></span>

<span data-ttu-id="177ed-108">**DWORD** (хранится в формате **Long**)</span><span class="sxs-lookup"><span data-stu-id="177ed-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="177ed-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="177ed-109">VT\_I4</span></span>

<span data-ttu-id="177ed-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="177ed-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="177ed-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="177ed-111">Remarks</span></span>

<span data-ttu-id="177ed-112">Константа **мфнетсаурце \_ максбуффертимемс** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="177ed-112">The constant **MFNETSOURCE\_MAXBUFFERTIMEMS** defines the GUID for this property key.</span></span> <span data-ttu-id="177ed-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="177ed-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="177ed-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="177ed-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="177ed-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="177ed-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="177ed-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="177ed-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="177ed-117">Значение этого свойства по умолчанию равно 40 000 миллисекундам.</span><span class="sxs-lookup"><span data-stu-id="177ed-117">The default value of this property is 40,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="177ed-118">Требования</span><span class="sxs-lookup"><span data-stu-id="177ed-118">Requirements</span></span>



| <span data-ttu-id="177ed-119">Требование</span><span class="sxs-lookup"><span data-stu-id="177ed-119">Requirement</span></span> | <span data-ttu-id="177ed-120">Значение</span><span class="sxs-lookup"><span data-stu-id="177ed-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="177ed-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="177ed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="177ed-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="177ed-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="177ed-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="177ed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="177ed-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="177ed-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="177ed-125">Header</span><span class="sxs-lookup"><span data-stu-id="177ed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="177ed-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="177ed-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177ed-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="177ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177ed-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="177ed-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="177ed-129">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="177ed-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="177ed-130">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="177ed-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




