---
description: Хранит указатель IUnknown класса, реализующего интерфейс Имфсслцертификатеманажер.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: Свойство MFNETSOURCE_SSLCERTIFICATE_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710811"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a><span data-ttu-id="792dc-103">МФНЕТСАУРЦЕ \_ сслцертификате \_ Manager, свойство</span><span class="sxs-lookup"><span data-stu-id="792dc-103">MFNETSOURCE\_SSLCERTIFICATE\_MANAGER property</span></span>

<span data-ttu-id="792dc-104">Хранит указатель **IUnknown** класса, реализующего интерфейс [**имфсслцертификатеманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) .</span><span class="sxs-lookup"><span data-stu-id="792dc-104">Stores the **IUnknown** pointer of the class that implements the [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) interface.</span></span> <span data-ttu-id="792dc-105">Реализация клиента предоставляет методы для получения SSL-сертификата клиента, когда он запрашивается сервером.</span><span class="sxs-lookup"><span data-stu-id="792dc-105">The client implemention provides methods to get the client SSL certificate when it is requested by the server.</span></span>



<span data-ttu-id="792dc-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="792dc-106">Data type</span></span>

<span data-ttu-id="792dc-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="792dc-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="792dc-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="792dc-108">PROPVARIANT member</span></span>

<span data-ttu-id="792dc-109">**Указатель IUnknown**</span><span class="sxs-lookup"><span data-stu-id="792dc-109">**IUnknown pointer**</span></span>

<span data-ttu-id="792dc-110">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="792dc-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="792dc-111">**пунквал**</span><span class="sxs-lookup"><span data-stu-id="792dc-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="792dc-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="792dc-112">Remarks</span></span>

<span data-ttu-id="792dc-113">Константа **мфнетсаурце \_ сслцертификате \_ Manager** определяет идентификатор GUID для ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="792dc-113">The **MFNETSOURCE\_SSLCERTIFICATE\_MANAGER** constant defines the GUID for the property key.</span></span> <span data-ttu-id="792dc-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="792dc-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="792dc-115">Чтобы задать это свойство в сетевом источнике, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="792dc-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="792dc-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="792dc-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="792dc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="792dc-117">Requirements</span></span>



| <span data-ttu-id="792dc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="792dc-118">Requirement</span></span> | <span data-ttu-id="792dc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="792dc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="792dc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="792dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="792dc-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="792dc-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="792dc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="792dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="792dc-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="792dc-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="792dc-124">Header</span><span class="sxs-lookup"><span data-stu-id="792dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="792dc-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="792dc-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="792dc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="792dc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792dc-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="792dc-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="792dc-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="792dc-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




