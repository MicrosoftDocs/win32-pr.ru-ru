---
description: Хранит массив байтов, представляющий лицензию DRM, связанную с потоком байтов.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: Свойство MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810996"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a><span data-ttu-id="20cf2-103">МФНЕТСАУРЦЕ \_ дрмнет \_ , \_ свойство представления лицензии</span><span class="sxs-lookup"><span data-stu-id="20cf2-103">MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION property</span></span>

<span data-ttu-id="20cf2-104">Хранит массив байтов, представляющий лицензию DRM, связанную с потоком байтов.</span><span class="sxs-lookup"><span data-stu-id="20cf2-104">Stores an array of bytes that represents the DRM license associated with the byte stream.</span></span>



<span data-ttu-id="20cf2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="20cf2-105">Data type</span></span>

<span data-ttu-id="20cf2-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="20cf2-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="20cf2-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="20cf2-107">PROPVARIANT member</span></span>

<span data-ttu-id="20cf2-108">Массив байтов (**BLOB**)</span><span class="sxs-lookup"><span data-stu-id="20cf2-108">Byte array (**BLOB**)</span></span>

<span data-ttu-id="20cf2-109">\_большой двоичный объект VT</span><span class="sxs-lookup"><span data-stu-id="20cf2-109">VT\_BLOB</span></span>

<span data-ttu-id="20cf2-110">**объекте**</span><span class="sxs-lookup"><span data-stu-id="20cf2-110">**blob**</span></span>



## <a name="remarks"></a><span data-ttu-id="20cf2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20cf2-111">Remarks</span></span>

<span data-ttu-id="20cf2-112">В **\_ \_ \_ представлении лицензии Constant мфнетсаурце дрмнет** определяется идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="20cf2-112">The constant **MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION** defines the GUID for this property key.</span></span> <span data-ttu-id="20cf2-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="20cf2-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="20cf2-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="20cf2-114">This property is read-only.</span></span> <span data-ttu-id="20cf2-115">Чтобы получить значение свойства из потока сетевого байта, вызовите метод **ипропертисторе:: GetValue** и передайте структуру **PROPERTYKEY** в параметре *Key* .</span><span class="sxs-lookup"><span data-stu-id="20cf2-115">To get the property value from the network byte stream, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="20cf2-116">Члену **fmtid** объекта **PROPERTYKEY** должно быть присвоено значение GUID свойства.</span><span class="sxs-lookup"><span data-stu-id="20cf2-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="20cf2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="20cf2-117">Requirements</span></span>



| <span data-ttu-id="20cf2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="20cf2-118">Requirement</span></span> | <span data-ttu-id="20cf2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="20cf2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20cf2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20cf2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="20cf2-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20cf2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="20cf2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20cf2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="20cf2-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20cf2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="20cf2-124">Header</span><span class="sxs-lookup"><span data-stu-id="20cf2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="20cf2-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="20cf2-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20cf2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20cf2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20cf2-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20cf2-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="20cf2-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20cf2-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




