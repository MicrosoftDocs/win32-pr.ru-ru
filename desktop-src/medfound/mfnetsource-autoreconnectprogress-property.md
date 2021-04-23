---
description: Число попыток повторного подключения сетевого источника к сети.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Свойство MFNETSOURCE_AUTORECONNECTPROGRESS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711273"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a><span data-ttu-id="6ed95-103">МФНЕТСАУРЦЕ \_ аутореконнектпрогресс, свойство</span><span class="sxs-lookup"><span data-stu-id="6ed95-103">MFNETSOURCE\_AUTORECONNECTPROGRESS property</span></span>

<span data-ttu-id="6ed95-104">Число попыток повторного подключения сетевого источника к сети.</span><span class="sxs-lookup"><span data-stu-id="6ed95-104">The number of times the network source has attempted to reconnect to the network.</span></span>



<span data-ttu-id="6ed95-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6ed95-105">Data type</span></span>

<span data-ttu-id="6ed95-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="6ed95-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6ed95-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="6ed95-107">PROPVARIANT member</span></span>

<span data-ttu-id="6ed95-108">**DWORD** (хранится в формате **Long**)</span><span class="sxs-lookup"><span data-stu-id="6ed95-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="6ed95-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6ed95-109">VT\_I4</span></span>

<span data-ttu-id="6ed95-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="6ed95-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6ed95-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ed95-111">Remarks</span></span>

<span data-ttu-id="6ed95-112">Константа **мфнетсаурце \_ аутореконнектпрогресс** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="6ed95-112">The constant **MFNETSOURCE\_AUTORECONNECTPROGRESS** defines the GUID for this property key.</span></span> <span data-ttu-id="6ed95-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="6ed95-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6ed95-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6ed95-114">This property is read-only.</span></span> <span data-ttu-id="6ed95-115">Чтобы получить это свойство, выполните запрос к источнику сети для интерфейса **ипропертисторе** и вызовите метод **Ипропертисторе:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="6ed95-115">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ed95-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6ed95-116">Requirements</span></span>



| <span data-ttu-id="6ed95-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6ed95-117">Requirement</span></span> | <span data-ttu-id="6ed95-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6ed95-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed95-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ed95-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed95-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ed95-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ed95-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ed95-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed95-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ed95-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ed95-123">Header</span><span class="sxs-lookup"><span data-stu-id="6ed95-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ed95-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ed95-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ed95-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ed95-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed95-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ed95-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6ed95-127">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="6ed95-127">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="6ed95-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ed95-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




