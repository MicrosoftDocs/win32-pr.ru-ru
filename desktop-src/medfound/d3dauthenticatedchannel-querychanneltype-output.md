---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY чаннелтипе.
ms.assetid: 547f7f26-2b9d-48b1-97cc-84a2202c3900
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3120669da69f13359f49d8b8c38ed7d3e211a8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423558"
---
# <a name="d3dauthenticatedchannel_querychanneltype_output-structure"></a><span data-ttu-id="2c9c5-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куеричаннелтипе</span><span class="sxs-lookup"><span data-stu-id="2c9c5-103">D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="2c9c5-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ чаннелтипе**](d3dauthenticatedquery-channeltype.md) .</span><span class="sxs-lookup"><span data-stu-id="2c9c5-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) query.</span></span>

<span data-ttu-id="2c9c5-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="2c9c5-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c9c5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c9c5-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DAUTHENTICATEDCHANNELTYPE          ChannelType;
} D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="2c9c5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="2c9c5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c9c5-108">**Выходные данные**</span><span class="sxs-lookup"><span data-stu-id="2c9c5-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="2c9c5-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="2c9c5-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="2c9c5-110">**чаннелтипе**</span><span class="sxs-lookup"><span data-stu-id="2c9c5-110">**ChannelType**</span></span>
</dt> <dd>

<span data-ttu-id="2c9c5-111">Значение [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) , указывающее тип канала.</span><span class="sxs-lookup"><span data-stu-id="2c9c5-111">A [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) value that specifies the channel type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c9c5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2c9c5-112">Requirements</span></span>



| <span data-ttu-id="2c9c5-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2c9c5-113">Requirement</span></span> | <span data-ttu-id="2c9c5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2c9c5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c9c5-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c9c5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2c9c5-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2c9c5-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c9c5-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c9c5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2c9c5-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c9c5-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2c9c5-119">Header</span><span class="sxs-lookup"><span data-stu-id="2c9c5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c9c5-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c9c5-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c9c5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c9c5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c9c5-122">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="2c9c5-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2c9c5-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="2c9c5-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




