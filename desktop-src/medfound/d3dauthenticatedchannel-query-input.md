---
description: 'Содержит входные данные для метода IDirect3DAuthenticatedChannel9:: Query.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: Структура D3DAUTHENTICATEDCHANNEL_QUERY_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262805"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a><span data-ttu-id="f0196-103">\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="f0196-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT structure</span></span>

<span data-ttu-id="f0196-104">Содержит входные данные для метода [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="f0196-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0196-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0196-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a><span data-ttu-id="f0196-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f0196-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0196-107">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="f0196-107">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="f0196-108">Идентификатор GUID, указывающий запрос.</span><span class="sxs-lookup"><span data-stu-id="f0196-108">A GUID that specifies the query.</span></span> <span data-ttu-id="f0196-109">Список значений см. в разделе [запросы защита содержимого](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="f0196-109">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0196-110">**СПРАВИТЬСЯ**</span><span class="sxs-lookup"><span data-stu-id="f0196-110">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="f0196-111">Маркер для аутентифицированного канала.</span><span class="sxs-lookup"><span data-stu-id="f0196-111">A handle to the authenticated channel.</span></span> <span data-ttu-id="f0196-112">Чтобы получить этот маркер, вызовите метод [**IDirect3DDevice9Video:: креатеаусентикатедчаннел**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="f0196-112">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="f0196-113">**UINT**</span><span class="sxs-lookup"><span data-stu-id="f0196-113">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="f0196-114">Порядковый номер запроса.</span><span class="sxs-lookup"><span data-stu-id="f0196-114">The query sequence number.</span></span> <span data-ttu-id="f0196-115">В начале сеанса создайте криптографически защищенное 32-разрядное случайное число, которое будет использоваться в качестве начального порядкового номера.</span><span class="sxs-lookup"><span data-stu-id="f0196-115">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="f0196-116">Для каждого запроса увеличьте порядковый номер на 1.</span><span class="sxs-lookup"><span data-stu-id="f0196-116">For each query, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0196-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f0196-117">Requirements</span></span>



| <span data-ttu-id="f0196-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f0196-118">Requirement</span></span> | <span data-ttu-id="f0196-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f0196-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0196-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0196-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0196-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f0196-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f0196-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0196-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0196-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0196-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f0196-124">Header</span><span class="sxs-lookup"><span data-stu-id="f0196-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0196-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0196-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0196-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0196-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0196-127">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="f0196-127">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="f0196-128">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="f0196-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




