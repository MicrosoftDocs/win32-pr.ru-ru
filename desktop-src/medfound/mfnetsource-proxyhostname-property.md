---
description: Указывает имя узла прокси-сервера.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: Свойство MFNETSOURCE_PROXYHOSTNAME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711210"
---
# <a name="mfnetsource_proxyhostname-property"></a><span data-ttu-id="f8372-103">МФНЕТСАУРЦЕ \_ проксихостнаме, свойство</span><span class="sxs-lookup"><span data-stu-id="f8372-103">MFNETSOURCE\_PROXYHOSTNAME property</span></span>

<span data-ttu-id="f8372-104">Указывает имя узла прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="f8372-104">Specifies the host name of the proxy server.</span></span>



<span data-ttu-id="f8372-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f8372-105">Data type</span></span>

<span data-ttu-id="f8372-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="f8372-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f8372-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="f8372-107">PROPVARIANT member</span></span>

<span data-ttu-id="f8372-108">Строка расширенных символов (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="f8372-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="f8372-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f8372-109">VT\_LPWSTR</span></span>

<span data-ttu-id="f8372-110">**пвсзвал**</span><span class="sxs-lookup"><span data-stu-id="f8372-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f8372-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8372-111">Remarks</span></span>

<span data-ttu-id="f8372-112">Константа **мфнетсаурце \_ проксихостнаме** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="f8372-112">The constant **MFNETSOURCE\_PROXYHOSTNAME** defines the GUID for this property key.</span></span> <span data-ttu-id="f8372-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="f8372-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f8372-114">Приложения могут использовать это свойство для настройки локатора прокси-сервера по умолчанию при создании объекта локатора прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="f8372-114">Applications can use this property to configure the default proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="f8372-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в параметре *ппроксиконфиг* функции [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="f8372-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="f8372-116">Это свойство должно быть задано приложением, если локатор прокси-сервера настроен для выполнения в ручном режиме.</span><span class="sxs-lookup"><span data-stu-id="f8372-116">This property must be set by the application when the proxy locator is configured to operate in the manual mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8372-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f8372-117">Requirements</span></span>



| <span data-ttu-id="f8372-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f8372-118">Requirement</span></span> | <span data-ttu-id="f8372-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f8372-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8372-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8372-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f8372-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8372-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f8372-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8372-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f8372-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8372-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8372-124">Header</span><span class="sxs-lookup"><span data-stu-id="f8372-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8372-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8372-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8372-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8372-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f8372-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f8372-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f8372-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f8372-129">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="f8372-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




