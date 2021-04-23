---
description: Задает параметр конфигурации для локатора прокси-сервера по умолчанию.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: Свойство MFNETSOURCE_PROXYSETTINGS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155555"
---
# <a name="mfnetsource_proxysettings-property"></a><span data-ttu-id="79d13-103">МФНЕТСАУРЦЕ \_ проксисеттингс, свойство</span><span class="sxs-lookup"><span data-stu-id="79d13-103">MFNETSOURCE\_PROXYSETTINGS property</span></span>

<span data-ttu-id="79d13-104">Задает параметр конфигурации для локатора прокси-сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79d13-104">Specifies the configuration setting for the default proxy locator.</span></span> <span data-ttu-id="79d13-105">Значение этого свойства является членом перечисления [**мфнет \_ проксисеттингс**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) .</span><span class="sxs-lookup"><span data-stu-id="79d13-105">The value of this property is a member of the [**MFNET\_PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) enumeration.</span></span>



<span data-ttu-id="79d13-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="79d13-106">Data type</span></span>

<span data-ttu-id="79d13-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="79d13-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="79d13-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="79d13-108">PROPVARIANT member</span></span>

<span data-ttu-id="79d13-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="79d13-109">**LONG**</span></span>

<span data-ttu-id="79d13-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="79d13-110">VT\_I4</span></span>

<span data-ttu-id="79d13-111">**лвал**</span><span class="sxs-lookup"><span data-stu-id="79d13-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="79d13-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79d13-112">Remarks</span></span>

<span data-ttu-id="79d13-113">Константа **мфнетсаурце \_ проксисеттингс** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="79d13-113">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="79d13-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="79d13-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="79d13-115">Приложения могут использовать это свойство для настройки локатора прокси при создании объекта-посредника по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79d13-115">Applications can use this property to configure the proxy locator when creating the default proxy locator object.</span></span> <span data-ttu-id="79d13-116">Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="79d13-116">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="79d13-117">Требования</span><span class="sxs-lookup"><span data-stu-id="79d13-117">Requirements</span></span>



| <span data-ttu-id="79d13-118">Требование</span><span class="sxs-lookup"><span data-stu-id="79d13-118">Requirement</span></span> | <span data-ttu-id="79d13-119">Значение</span><span class="sxs-lookup"><span data-stu-id="79d13-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79d13-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79d13-120">Minimum supported client</span></span><br/> | <span data-ttu-id="79d13-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79d13-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="79d13-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79d13-122">Minimum supported server</span></span><br/> | <span data-ttu-id="79d13-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79d13-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="79d13-124">Header</span><span class="sxs-lookup"><span data-stu-id="79d13-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="79d13-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="79d13-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79d13-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79d13-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d13-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79d13-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="79d13-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79d13-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="79d13-129">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="79d13-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




