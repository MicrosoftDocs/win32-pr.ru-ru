---
description: Связывает сеанс шифрования с устройством декодера DirectX Video Acceleration 2 (ДКСВА-2) и устройством Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656095"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a><span data-ttu-id="eeea8-103">D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="eeea8-103">D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION</span></span>

<span data-ttu-id="eeea8-104">Связывает сеанс шифрования с устройством декодера DirectX Video Acceleration 2 (ДКСВА-2) и устройством Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eeea8-104">Associates a cryptographic session with a DirectX Video Acceleration 2 (DXVA-2) decoder device and a Direct3D device.</span></span>



| <span data-ttu-id="eeea8-105">Требование</span><span class="sxs-lookup"><span data-stu-id="eeea8-105">Requirement</span></span> | <span data-ttu-id="eeea8-106">Значение</span><span class="sxs-lookup"><span data-stu-id="eeea8-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeea8-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="eeea8-107">Command GUID</span></span> | <span data-ttu-id="eeea8-108">**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="eeea8-108">**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**</span></span>                                                              |
| <span data-ttu-id="eeea8-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="eeea8-109">Input data</span></span>   | [<span data-ttu-id="eeea8-110">**D3DAUTHENTICATEDCHANNEL \_ конфигурекриптосессион**</span><span class="sxs-lookup"><span data-stu-id="eeea8-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION**</span></span>](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a><span data-ttu-id="eeea8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eeea8-111">Remarks</span></span>

<span data-ttu-id="eeea8-112">После отправки этой команды можно отправить запрос [D3DAUTHENTICATEDQUERY \_ аутпутид](d3dauthenticatedquery-outputid.md) , чтобы узнать, какие выходные данные видео связаны с сеансом шифрования.</span><span class="sxs-lookup"><span data-stu-id="eeea8-112">After this command is sent, you can send the [D3DAUTHENTICATEDQUERY\_OUTPUTID](d3dauthenticatedquery-outputid.md) query to find out which video outputs are associated with the cryptographic session.</span></span>

<span data-ttu-id="eeea8-113">Эта команда поддерживается следующими типами каналов:</span><span class="sxs-lookup"><span data-stu-id="eeea8-113">The following channel types support this command:</span></span>

-   <span data-ttu-id="eeea8-114">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="eeea8-114">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="eeea8-115">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="eeea8-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="eeea8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="eeea8-116">Requirements</span></span>



| <span data-ttu-id="eeea8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="eeea8-117">Requirement</span></span> | <span data-ttu-id="eeea8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="eeea8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeea8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eeea8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eeea8-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eeea8-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eeea8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eeea8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eeea8-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eeea8-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="eeea8-123">Header</span><span class="sxs-lookup"><span data-stu-id="eeea8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeea8-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeea8-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeea8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eeea8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeea8-126">Защита содержимого команды</span><span class="sxs-lookup"><span data-stu-id="eeea8-126">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="eeea8-127">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="eeea8-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="eeea8-128">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="eeea8-128">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




