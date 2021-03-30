---
description: Количество попыток повторного подключения сетевого источника к серверу и возобновления потоковой передачи при потере соединения.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: Свойство MFNETSOURCE_AUTORECONNECTLIMIT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac2a81cb4d47d8113059924877670458ac22ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811002"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a><span data-ttu-id="578c7-103">МФНЕТСАУРЦЕ \_ аутореконнектлимит, свойство</span><span class="sxs-lookup"><span data-stu-id="578c7-103">MFNETSOURCE\_AUTORECONNECTLIMIT property</span></span>

<span data-ttu-id="578c7-104">Количество попыток повторного подключения сетевого источника к серверу и возобновления потоковой передачи при потере соединения.</span><span class="sxs-lookup"><span data-stu-id="578c7-104">The number of times the network source tries to reconnect to the server and resume streaming if the connection is lost.</span></span>



<span data-ttu-id="578c7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="578c7-105">Data type</span></span>

<span data-ttu-id="578c7-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="578c7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="578c7-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="578c7-107">PROPVARIANT member</span></span>

<span data-ttu-id="578c7-108">**DWORD** (хранится в формате **Long**)</span><span class="sxs-lookup"><span data-stu-id="578c7-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="578c7-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="578c7-109">VT\_I4</span></span>

<span data-ttu-id="578c7-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="578c7-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="578c7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="578c7-111">Remarks</span></span>

<span data-ttu-id="578c7-112">Константа **мфнетсаурце \_ аутореконнектлимит** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="578c7-112">The constant **MFNETSOURCE\_AUTORECONNECTLIMIT** defines the GUID for this property key.</span></span> <span data-ttu-id="578c7-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="578c7-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="578c7-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="578c7-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="578c7-115">Чтобы задать свойство, передайте объект **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="578c7-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="578c7-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="578c7-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="578c7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="578c7-117">Requirements</span></span>



| <span data-ttu-id="578c7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="578c7-118">Requirement</span></span> | <span data-ttu-id="578c7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="578c7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="578c7-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="578c7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="578c7-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="578c7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="578c7-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="578c7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="578c7-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="578c7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="578c7-124">Header</span><span class="sxs-lookup"><span data-stu-id="578c7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="578c7-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="578c7-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="578c7-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="578c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578c7-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="578c7-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="578c7-128">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="578c7-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="578c7-129">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="578c7-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




