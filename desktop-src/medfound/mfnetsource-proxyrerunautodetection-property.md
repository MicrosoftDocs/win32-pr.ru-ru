---
description: Указывает, должен ли локатор прокси-сервера по умолчанию принудительно выполнять автоматическое обнаружение прокси-сервера.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: Свойство MFNETSOURCE_PROXYRERUNAUTODETECTION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544327"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a><span data-ttu-id="25c82-103">МФНЕТСАУРЦЕ \_ проксирерунаутодетектион, свойство</span><span class="sxs-lookup"><span data-stu-id="25c82-103">MFNETSOURCE\_PROXYRERUNAUTODETECTION property</span></span>

<span data-ttu-id="25c82-104">Указывает, должен ли локатор прокси-сервера по умолчанию принудительно выполнять автоматическое обнаружение прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="25c82-104">Specifies whether the default proxy locator should force proxy auto-detection.</span></span>



<span data-ttu-id="25c82-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="25c82-105">Data type</span></span>

<span data-ttu-id="25c82-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="25c82-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="25c82-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="25c82-107">PROPVARIANT member</span></span>

<span data-ttu-id="25c82-108">Логическое значение (**Long**)</span><span class="sxs-lookup"><span data-stu-id="25c82-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="25c82-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="25c82-109">VT\_I4</span></span>

<span data-ttu-id="25c82-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="25c82-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="25c82-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25c82-111">Remarks</span></span>

<span data-ttu-id="25c82-112">Константа **мфнетсаурце \_ проксисеттингс** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="25c82-112">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="25c82-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="25c82-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="25c82-114">Приложения могут использовать это свойство для настройки локатора прокси при создании прокси-объекта-локатора.</span><span class="sxs-lookup"><span data-stu-id="25c82-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="25c82-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="25c82-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="25c82-116">В режиме автоматического обнаружения локатор прокси-сервера использует механизм обнаружения прокси WinInet.</span><span class="sxs-lookup"><span data-stu-id="25c82-116">In auto-detect mode, the proxy locator uses the WinInet proxy detection mechanism.</span></span> <span data-ttu-id="25c82-117">Чтобы принудительно включить автоматическое обнаружение, установите значение 0.</span><span class="sxs-lookup"><span data-stu-id="25c82-117">To force auto-detection, set the value to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c82-118">Требования</span><span class="sxs-lookup"><span data-stu-id="25c82-118">Requirements</span></span>



| <span data-ttu-id="25c82-119">Требование</span><span class="sxs-lookup"><span data-stu-id="25c82-119">Requirement</span></span> | <span data-ttu-id="25c82-120">Значение</span><span class="sxs-lookup"><span data-stu-id="25c82-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25c82-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25c82-121">Minimum supported client</span></span><br/> | <span data-ttu-id="25c82-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25c82-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="25c82-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25c82-123">Minimum supported server</span></span><br/> | <span data-ttu-id="25c82-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25c82-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="25c82-125">Header</span><span class="sxs-lookup"><span data-stu-id="25c82-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="25c82-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="25c82-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25c82-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25c82-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c82-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25c82-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="25c82-129">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25c82-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="25c82-130">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="25c82-130">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




