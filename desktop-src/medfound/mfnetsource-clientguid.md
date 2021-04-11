---
description: Уникальный идентификатор, по которому сервер идентифицирует клиента.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Свойство MFNETSOURCE_CLIENTGUID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154963"
---
# <a name="mfnetsource_clientguid-property"></a><span data-ttu-id="a57dd-103">МФНЕТСАУРЦЕ \_ клиентгуид, свойство</span><span class="sxs-lookup"><span data-stu-id="a57dd-103">MFNETSOURCE\_CLIENTGUID property</span></span>

<span data-ttu-id="a57dd-104">Уникальный идентификатор, по которому сервер идентифицирует клиента.</span><span class="sxs-lookup"><span data-stu-id="a57dd-104">Unique identifier by which the server identifies the client.</span></span>



<span data-ttu-id="a57dd-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a57dd-105">Data type</span></span>

<span data-ttu-id="a57dd-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="a57dd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a57dd-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="a57dd-107">PROPVARIANT member</span></span>

<span data-ttu-id="a57dd-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a57dd-108">**GUID**</span></span>

<span data-ttu-id="a57dd-109">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="a57dd-109">VT\_CLSID</span></span>

<span data-ttu-id="a57dd-110">**пууид**</span><span class="sxs-lookup"><span data-stu-id="a57dd-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="a57dd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a57dd-111">Remarks</span></span>

<span data-ttu-id="a57dd-112">Константа **\_ клиентгуид мфнетсаурце** определяет идентификатор GUID для ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="a57dd-112">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="a57dd-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a57dd-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="a57dd-114">Чтобы задать это свойство в сетевом источнике, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="a57dd-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a57dd-115">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a57dd-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="a57dd-116">Если параметр не задан или задан как **GUID \_ NULL**, Microsoft Media Foundation создает анонимный идентификатор GUID для сеанса, гарантирующий конфиденциальность пользователя.</span><span class="sxs-lookup"><span data-stu-id="a57dd-116">If not set or set as **GUID\_NULL**, Microsoft Media Foundation generates an anonymous GUID per session that ensures the user's privacy.</span></span>

## <a name="requirements"></a><span data-ttu-id="a57dd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a57dd-117">Requirements</span></span>



| <span data-ttu-id="a57dd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a57dd-118">Requirement</span></span> | <span data-ttu-id="a57dd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a57dd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a57dd-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a57dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a57dd-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a57dd-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a57dd-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a57dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a57dd-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a57dd-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a57dd-124">Header</span><span class="sxs-lookup"><span data-stu-id="a57dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a57dd-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a57dd-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a57dd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a57dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57dd-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a57dd-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a57dd-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a57dd-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




