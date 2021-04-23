---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY енкриптионвхенакцессиблегуид.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8fa46095c5075b0a36ed691978b73de1e7b8cade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896573"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a><span data-ttu-id="a5630-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуид</span><span class="sxs-lookup"><span data-stu-id="a5630-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT structure</span></span>

<span data-ttu-id="a5630-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="a5630-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="a5630-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="a5630-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5630-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5630-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="a5630-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a5630-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5630-108">**\_ \_ Выходные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="a5630-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="a5630-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="a5630-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="a5630-110">**енкриптионгуидиндекс**</span><span class="sxs-lookup"><span data-stu-id="a5630-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a5630-111">Индекс GUID шифрования.</span><span class="sxs-lookup"><span data-stu-id="a5630-111">The index of the encryption GUID.</span></span>

</dd> <dt>

<span data-ttu-id="a5630-112">**енкриптионгуид**</span><span class="sxs-lookup"><span data-stu-id="a5630-112">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="a5630-113">Идентификатор GUID, указывающий поддерживаемый тип шифрования.</span><span class="sxs-lookup"><span data-stu-id="a5630-113">A GUID that specifies a supported encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5630-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a5630-114">Requirements</span></span>



| <span data-ttu-id="a5630-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a5630-115">Requirement</span></span> | <span data-ttu-id="a5630-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a5630-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5630-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5630-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5630-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a5630-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a5630-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5630-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5630-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5630-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a5630-121">Header</span><span class="sxs-lookup"><span data-stu-id="a5630-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5630-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5630-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5630-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5630-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5630-124">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="a5630-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a5630-125">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a5630-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




