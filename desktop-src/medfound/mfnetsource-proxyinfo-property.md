---
description: Хранит имя узла и порт прокси-сервера, используемого сетевым источником.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: Свойство MFNETSOURCE_PROXYINFO (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712251"
---
# <a name="mfnetsource_proxyinfo-property"></a><span data-ttu-id="10fb2-103">МФНЕТСАУРЦЕ \_ проксинфо, свойство</span><span class="sxs-lookup"><span data-stu-id="10fb2-103">MFNETSOURCE\_PROXYINFO property</span></span>

<span data-ttu-id="10fb2-104">Хранит имя узла и порт прокси-сервера, используемого сетевым источником.</span><span class="sxs-lookup"><span data-stu-id="10fb2-104">Stores the host name and the port of the proxy server used by the network source.</span></span>



<span data-ttu-id="10fb2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="10fb2-105">Data type</span></span>

<span data-ttu-id="10fb2-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="10fb2-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="10fb2-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="10fb2-107">PROPVARIANT member</span></span>

<span data-ttu-id="10fb2-108">Строка расширенных символов (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="10fb2-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="10fb2-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="10fb2-109">VT\_LPWSTR</span></span>

<span data-ttu-id="10fb2-110">**пвсзвал**</span><span class="sxs-lookup"><span data-stu-id="10fb2-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="10fb2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10fb2-111">Remarks</span></span>

<span data-ttu-id="10fb2-112">Константа **мфнетсаурце \_ проксинфо** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="10fb2-112">The constant **MFNETSOURCE\_PROXYINFO** defines the GUID for this property key.</span></span> <span data-ttu-id="10fb2-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="10fb2-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="10fb2-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="10fb2-114">This property is read-only.</span></span> <span data-ttu-id="10fb2-115">Чтобы получить значение свойства из сетевого источника, вызовите метод **ипропертисторе:: GetValue** и передайте структуру **PROPERTYKEY** в параметре *Key* .</span><span class="sxs-lookup"><span data-stu-id="10fb2-115">To get the property value from the network source, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="10fb2-116">Члену **fmtid** объекта **PROPERTYKEY** должно быть присвоено значение GUID свойства.</span><span class="sxs-lookup"><span data-stu-id="10fb2-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fb2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="10fb2-117">Requirements</span></span>



| <span data-ttu-id="10fb2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="10fb2-118">Requirement</span></span> | <span data-ttu-id="10fb2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="10fb2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10fb2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10fb2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10fb2-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10fb2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="10fb2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10fb2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10fb2-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10fb2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="10fb2-124">Header</span><span class="sxs-lookup"><span data-stu-id="10fb2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10fb2-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="10fb2-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fb2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10fb2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fb2-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10fb2-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="10fb2-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10fb2-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="10fb2-129">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="10fb2-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




