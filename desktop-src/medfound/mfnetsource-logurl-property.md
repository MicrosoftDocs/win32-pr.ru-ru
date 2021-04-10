---
description: Список URL-адресов, на которые сетевой источник будет передавать данные журнала.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: Свойство MFNETSOURCE_LOGURL (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154627"
---
# <a name="mfnetsource_logurl-property"></a><span data-ttu-id="80158-103">МФНЕТСАУРЦЕ \_ логурл, свойство</span><span class="sxs-lookup"><span data-stu-id="80158-103">MFNETSOURCE\_LOGURL property</span></span>

<span data-ttu-id="80158-104">Список URL-адресов, на которые сетевой источник будет передавать данные журнала.</span><span class="sxs-lookup"><span data-stu-id="80158-104">List of URLs to which the network source will send logging information.</span></span>



<span data-ttu-id="80158-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="80158-105">Data type</span></span>

<span data-ttu-id="80158-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="80158-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="80158-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="80158-107">PROPVARIANT member</span></span>

<span data-ttu-id="80158-108">Массив строк расширенных символов (**калпвстр**)</span><span class="sxs-lookup"><span data-stu-id="80158-108">Array of wide-character strings (**CALPWSTR**)</span></span>

<span data-ttu-id="80158-109">VT \_ Векторная \| \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="80158-109">VT\_VECTOR \| VT\_LPWSTR</span></span>

<span data-ttu-id="80158-110">**калпвстр**</span><span class="sxs-lookup"><span data-stu-id="80158-110">**calpwstr**</span></span>



## <a name="remarks"></a><span data-ttu-id="80158-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80158-111">Remarks</span></span>

<span data-ttu-id="80158-112">Константа **мфнетсаурце \_ логурл** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="80158-112">The constant **MFNETSOURCE\_LOGURL** defines the GUID for this property key.</span></span> <span data-ttu-id="80158-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="80158-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="80158-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="80158-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="80158-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="80158-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="80158-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="80158-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80158-117">Требования</span><span class="sxs-lookup"><span data-stu-id="80158-117">Requirements</span></span>



| <span data-ttu-id="80158-118">Требование</span><span class="sxs-lookup"><span data-stu-id="80158-118">Requirement</span></span> | <span data-ttu-id="80158-119">Значение</span><span class="sxs-lookup"><span data-stu-id="80158-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80158-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80158-120">Minimum supported client</span></span><br/> | <span data-ttu-id="80158-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80158-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="80158-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80158-122">Minimum supported server</span></span><br/> | <span data-ttu-id="80158-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80158-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="80158-124">Header</span><span class="sxs-lookup"><span data-stu-id="80158-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="80158-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="80158-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80158-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80158-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80158-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80158-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="80158-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80158-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




