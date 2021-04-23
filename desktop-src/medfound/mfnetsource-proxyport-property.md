---
description: Указывает номер порта прокси-сервера.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: Свойство MFNETSOURCE_PROXYPORT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263613"
---
# <a name="mfnetsource_proxyport-property"></a><span data-ttu-id="2d2e4-103">МФНЕТСАУРЦЕ \_ проксипорт, свойство</span><span class="sxs-lookup"><span data-stu-id="2d2e4-103">MFNETSOURCE\_PROXYPORT property</span></span>

<span data-ttu-id="2d2e4-104">Указывает номер порта прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2d2e4-104">Specifies the port number of the proxy server.</span></span>



<span data-ttu-id="2d2e4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2d2e4-105">Data type</span></span>

<span data-ttu-id="2d2e4-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="2d2e4-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2d2e4-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="2d2e4-107">PROPVARIANT member</span></span>

<span data-ttu-id="2d2e4-108">**DWORD** (хранится в формате **Long**)</span><span class="sxs-lookup"><span data-stu-id="2d2e4-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="2d2e4-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2d2e4-109">VT\_I4</span></span>

<span data-ttu-id="2d2e4-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="2d2e4-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2d2e4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d2e4-111">Remarks</span></span>

<span data-ttu-id="2d2e4-112">Константа **мфнетсаурце \_ проксипорт** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="2d2e4-112">The constant **MFNETSOURCE\_PROXYPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="2d2e4-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2d2e4-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="2d2e4-114">Приложения могут использовать это свойство для настройки локатора прокси при создании прокси-объекта-локатора.</span><span class="sxs-lookup"><span data-stu-id="2d2e4-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="2d2e4-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="2d2e4-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="2d2e4-116">Если это свойство не задано для HTTP, по умолчанию локатор прокси-сервера использует значение 80.</span><span class="sxs-lookup"><span data-stu-id="2d2e4-116">If this property is not set for HTTP, then by default the proxy locator uses a value of 80.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d2e4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2d2e4-117">Requirements</span></span>



| <span data-ttu-id="2d2e4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2d2e4-118">Requirement</span></span> | <span data-ttu-id="2d2e4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2d2e4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2e4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d2e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2d2e4-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d2e4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2d2e4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d2e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2d2e4-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d2e4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2d2e4-124">Header</span><span class="sxs-lookup"><span data-stu-id="2d2e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d2e4-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d2e4-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d2e4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d2e4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2e4-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2d2e4-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2d2e4-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2d2e4-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2d2e4-129">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="2d2e4-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




