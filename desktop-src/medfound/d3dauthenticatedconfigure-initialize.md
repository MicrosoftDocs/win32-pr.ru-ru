---
description: Инициализирует аутентифицированный канал.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692055"
---
# <a name="d3dauthenticatedconfigure_initialize"></a><span data-ttu-id="95b23-103">\_Инициализация D3DAUTHENTICATEDCONFIGURE</span><span class="sxs-lookup"><span data-stu-id="95b23-103">D3DAUTHENTICATEDCONFIGURE\_INITIALIZE</span></span>

<span data-ttu-id="95b23-104">Инициализирует аутентифицированный канал.</span><span class="sxs-lookup"><span data-stu-id="95b23-104">Initializes the authenticated channel.</span></span>



| <span data-ttu-id="95b23-105">Требование</span><span class="sxs-lookup"><span data-stu-id="95b23-105">Requirement</span></span> | <span data-ttu-id="95b23-106">Значение</span><span class="sxs-lookup"><span data-stu-id="95b23-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b23-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="95b23-107">Command GUID</span></span> | <span data-ttu-id="95b23-108">**\_Инициализация D3DAUTHENTICATEDCONFIGURE**</span><span class="sxs-lookup"><span data-stu-id="95b23-108">**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**</span></span>                                                           |
| <span data-ttu-id="95b23-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="95b23-109">Input data</span></span>   | [<span data-ttu-id="95b23-110">**D3DAUTHENTICATEDCHANNEL \_ конфигуреинитиализе**</span><span class="sxs-lookup"><span data-stu-id="95b23-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE**</span></span>](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a><span data-ttu-id="95b23-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95b23-111">Remarks</span></span>

<span data-ttu-id="95b23-112">Отправить эту команду один раз в начале сеанса.</span><span class="sxs-lookup"><span data-stu-id="95b23-112">Send this command once, at the start of the session.</span></span> <span data-ttu-id="95b23-113">Эту команду можно отправить только один раз для каждого канала, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="95b23-113">This command can be sent only one time for each authenticated channel.</span></span> <span data-ttu-id="95b23-114">Входной порядковый номер для этой команды не учитывается.</span><span class="sxs-lookup"><span data-stu-id="95b23-114">The input sequence number is ignored for this command.</span></span>

<span data-ttu-id="95b23-115">Эта команда поддерживается следующими типами каналов:</span><span class="sxs-lookup"><span data-stu-id="95b23-115">The following channel types support this command:</span></span>

-   <span data-ttu-id="95b23-116">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="95b23-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="95b23-117">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="95b23-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="95b23-118">Требования</span><span class="sxs-lookup"><span data-stu-id="95b23-118">Requirements</span></span>



| <span data-ttu-id="95b23-119">Требование</span><span class="sxs-lookup"><span data-stu-id="95b23-119">Requirement</span></span> | <span data-ttu-id="95b23-120">Значение</span><span class="sxs-lookup"><span data-stu-id="95b23-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95b23-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95b23-121">Minimum supported client</span></span><br/> | <span data-ttu-id="95b23-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="95b23-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="95b23-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95b23-123">Minimum supported server</span></span><br/> | <span data-ttu-id="95b23-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="95b23-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="95b23-125">Header</span><span class="sxs-lookup"><span data-stu-id="95b23-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="95b23-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b23-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b23-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95b23-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b23-128">Защита содержимого команды</span><span class="sxs-lookup"><span data-stu-id="95b23-128">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="95b23-129">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="95b23-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="95b23-130">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="95b23-130">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




