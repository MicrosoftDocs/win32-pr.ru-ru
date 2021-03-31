---
description: Содержит указатель на интерфейс Имфнеткредентиалманажер.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: Свойство MFNETSOURCE_CREDENTIAL_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154962"
---
# <a name="mfnetsource_credential_manager-property"></a><span data-ttu-id="01047-103">\_Свойство диспетчера учетных данных мфнетсаурце \_</span><span class="sxs-lookup"><span data-stu-id="01047-103">MFNETSOURCE\_CREDENTIAL\_MANAGER property</span></span>

<span data-ttu-id="01047-104">Содержит указатель на интерфейс [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="01047-104">Contains a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="01047-105">Используйте это свойство, чтобы передать реализацию приложения [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) в сетевой источник.</span><span class="sxs-lookup"><span data-stu-id="01047-105">Use this property to pass the application's implementation of [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) to the network source.</span></span>



<span data-ttu-id="01047-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="01047-106">Data type</span></span>

<span data-ttu-id="01047-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="01047-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="01047-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="01047-108">PROPVARIANT member</span></span>

<span data-ttu-id="01047-109">Указатель **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="01047-109">**IUnknown** pointer</span></span>

<span data-ttu-id="01047-110">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="01047-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="01047-111">**пунквал**</span><span class="sxs-lookup"><span data-stu-id="01047-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="01047-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01047-112">Remarks</span></span>

<span data-ttu-id="01047-113">Константа **мфнетсаурце \_ Credential \_ Manager** определяет **идентификатор GUID** для ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="01047-113">The constant **MFNETSOURCE\_CREDENTIAL\_MANAGER** defines the **GUID** for the property key.</span></span> <span data-ttu-id="01047-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="01047-114">The property identifier (PID) is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="01047-115">Требования</span><span class="sxs-lookup"><span data-stu-id="01047-115">Requirements</span></span>



| <span data-ttu-id="01047-116">Требование</span><span class="sxs-lookup"><span data-stu-id="01047-116">Requirement</span></span> | <span data-ttu-id="01047-117">Значение</span><span class="sxs-lookup"><span data-stu-id="01047-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01047-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01047-118">Minimum supported client</span></span><br/> | <span data-ttu-id="01047-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01047-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="01047-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01047-120">Minimum supported server</span></span><br/> | <span data-ttu-id="01047-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01047-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="01047-122">Header</span><span class="sxs-lookup"><span data-stu-id="01047-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="01047-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="01047-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01047-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01047-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01047-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01047-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="01047-126">Проверка подлинности источника сети</span><span class="sxs-lookup"><span data-stu-id="01047-126">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> <dt>

[<span data-ttu-id="01047-127">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01047-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




