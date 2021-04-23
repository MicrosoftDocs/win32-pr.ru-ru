---
description: Диапазон допустимых UDP-портов, которые источник сети может использовать для получения потокового содержимого.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: Свойство MFNETSOURCE_UDP_PORT_RANGE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711208"
---
# <a name="mfnetsource_udp_port_range-property"></a><span data-ttu-id="a6d03-103">МФНЕТСАУРЦЕ \_ UDP \_ - \_ свойство диапазона портов</span><span class="sxs-lookup"><span data-stu-id="a6d03-103">MFNETSOURCE\_UDP\_PORT\_RANGE property</span></span>

<span data-ttu-id="a6d03-104">Диапазон допустимых UDP-портов, которые источник сети может использовать для получения потокового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a6d03-104">The range of valid UDP ports that the network source can use to receive streaming content.</span></span> <span data-ttu-id="a6d03-105">Значение этого свойства представляет собой строку в формате " *m*–*n* ", где *m* и *n* — номера портов.</span><span class="sxs-lookup"><span data-stu-id="a6d03-105">The value of this property is a string with the form " *m*–*n* " where *m* and *n* are port numbers.</span></span>



<span data-ttu-id="a6d03-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a6d03-106">Data type</span></span>

<span data-ttu-id="a6d03-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="a6d03-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a6d03-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="a6d03-108">PROPVARIANT member</span></span>

<span data-ttu-id="a6d03-109">Строка расширенных символов (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="a6d03-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="a6d03-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a6d03-110">VT\_LPWSTR</span></span>

<span data-ttu-id="a6d03-111">**пвсзвал**</span><span class="sxs-lookup"><span data-stu-id="a6d03-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a6d03-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6d03-112">Remarks</span></span>

<span data-ttu-id="a6d03-113">**\_ \_ \_ Диапазон UDP-портов Constant мфнетсаурце** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="a6d03-113">The constant **MFNETSOURCE\_UDP\_PORT\_RANGE** defines the GUID for this property key.</span></span> <span data-ttu-id="a6d03-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a6d03-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a6d03-115">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="a6d03-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a6d03-116">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="a6d03-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a6d03-117">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a6d03-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6d03-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a6d03-118">Requirements</span></span>



| <span data-ttu-id="a6d03-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a6d03-119">Requirement</span></span> | <span data-ttu-id="a6d03-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a6d03-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d03-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6d03-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6d03-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6d03-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6d03-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6d03-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6d03-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6d03-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a6d03-125">Header</span><span class="sxs-lookup"><span data-stu-id="a6d03-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6d03-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6d03-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6d03-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6d03-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d03-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6d03-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a6d03-129">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6d03-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




