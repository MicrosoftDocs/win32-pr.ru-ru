---
description: Позволяет процессу открывать общий ресурс или отключать процесс от открытия общих ресурсов.
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262801"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a><span data-ttu-id="12dcb-103">D3DAUTHENTICATEDCONFIGURE \_ шаредресаурце</span><span class="sxs-lookup"><span data-stu-id="12dcb-103">D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE</span></span>

<span data-ttu-id="12dcb-104">Позволяет процессу открывать общий ресурс или отключать процесс от открытия общих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12dcb-104">Enables a process to open a shared resource, or disables a process from opening shared resources.</span></span>



| <span data-ttu-id="12dcb-105">Требование</span><span class="sxs-lookup"><span data-stu-id="12dcb-105">Requirement</span></span> | <span data-ttu-id="12dcb-106">Значение</span><span class="sxs-lookup"><span data-stu-id="12dcb-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12dcb-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="12dcb-107">Command GUID</span></span> | <span data-ttu-id="12dcb-108">**D3DAUTHENTICATEDCONFIGURE \_ шаредресаурце**</span><span class="sxs-lookup"><span data-stu-id="12dcb-108">**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**</span></span>                                                               |
| <span data-ttu-id="12dcb-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="12dcb-109">Input data</span></span>   | [<span data-ttu-id="12dcb-110">**D3DAUTHENTICATEDCHANNEL \_ конфигурешаредресаурце**</span><span class="sxs-lookup"><span data-stu-id="12dcb-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE**</span></span>](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a><span data-ttu-id="12dcb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12dcb-111">Remarks</span></span>

<span data-ttu-id="12dcb-112">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="12dcb-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="12dcb-113">**\_Драйвер D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="12dcb-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_D3D9**</span></span>
-   <span data-ttu-id="12dcb-114">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="12dcb-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="12dcb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="12dcb-115">Requirements</span></span>



| <span data-ttu-id="12dcb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="12dcb-116">Requirement</span></span> | <span data-ttu-id="12dcb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="12dcb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12dcb-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12dcb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12dcb-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="12dcb-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="12dcb-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12dcb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12dcb-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="12dcb-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="12dcb-122">Header</span><span class="sxs-lookup"><span data-stu-id="12dcb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="12dcb-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="12dcb-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12dcb-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12dcb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12dcb-125">Защита содержимого команды</span><span class="sxs-lookup"><span data-stu-id="12dcb-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="12dcb-126">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="12dcb-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="12dcb-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="12dcb-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




