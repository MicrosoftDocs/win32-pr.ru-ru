---
description: Указывает, должен ли локатор прокси использовать прокси-сервер для локальных адресов.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: Свойство MFNETSOURCE_PROXYBYPASSFORLOCAL (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808045"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a><span data-ttu-id="f3c32-103">МФНЕТСАУРЦЕ \_ проксибипассфорлокал, свойство</span><span class="sxs-lookup"><span data-stu-id="f3c32-103">MFNETSOURCE\_PROXYBYPASSFORLOCAL property</span></span>

<span data-ttu-id="f3c32-104">Указывает, должен ли локатор прокси использовать прокси-сервер для локальных адресов.</span><span class="sxs-lookup"><span data-stu-id="f3c32-104">Specifies whether the proxy locator should use a proxy server for local addresses.</span></span>



<span data-ttu-id="f3c32-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f3c32-105">Data type</span></span>

<span data-ttu-id="f3c32-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="f3c32-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f3c32-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="f3c32-107">PROPVARIANT member</span></span>

<span data-ttu-id="f3c32-108">Логическое значение (**Long**)</span><span class="sxs-lookup"><span data-stu-id="f3c32-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="f3c32-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f3c32-109">VT\_I4</span></span>

<span data-ttu-id="f3c32-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="f3c32-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f3c32-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3c32-111">Remarks</span></span>

<span data-ttu-id="f3c32-112">Константа **мфнетсаурце \_ проксибипассфорлокал** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="f3c32-112">The constant **MFNETSOURCE\_PROXYBYPASSFORLOCAL** defines the GUID for this property key.</span></span> <span data-ttu-id="f3c32-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="f3c32-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f3c32-114">Приложения могут использовать это свойство для настройки локатора прокси при создании прокси-объекта-локатора.</span><span class="sxs-lookup"><span data-stu-id="f3c32-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="f3c32-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="f3c32-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="f3c32-116">Если прокси-сервер должен использоваться для локальных адресов, необходимо задать значение 0. в противном случае ненулевое значение настраивает локатор прокси-сервера по умолчанию, чтобы пропустить прокси-сервер для локальных адресов.</span><span class="sxs-lookup"><span data-stu-id="f3c32-116">The value must be set to 0 if the proxy server is to be used for local addresses; otherwise a nonzero value configures the default proxy locator to skip the proxy server for local addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c32-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f3c32-117">Requirements</span></span>



| <span data-ttu-id="f3c32-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f3c32-118">Requirement</span></span> | <span data-ttu-id="f3c32-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f3c32-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c32-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3c32-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c32-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3c32-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f3c32-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3c32-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c32-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3c32-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f3c32-124">Header</span><span class="sxs-lookup"><span data-stu-id="f3c32-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3c32-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c32-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3c32-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3c32-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c32-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3c32-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f3c32-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3c32-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f3c32-129">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="f3c32-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




