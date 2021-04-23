---
description: Содержит входные данные для \_ запроса D3DAUTHENTICATEDQUERY енкриптионвхенакцессиблегуид.
ms.assetid: 0e24e393-3f63-4c6f-aca1-f73ced3490ba
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1c4500d27577883f46d00580dcc7e306b4008cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423554"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_input-structure"></a><span data-ttu-id="9ee8a-103">\_ \_ Входная структура D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуид</span><span class="sxs-lookup"><span data-stu-id="9ee8a-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT structure</span></span>

<span data-ttu-id="9ee8a-104">Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="9ee8a-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="9ee8a-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="9ee8a-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee8a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ee8a-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                EncryptionGuidIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT;
```



## <a name="members"></a><span data-ttu-id="9ee8a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="9ee8a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ee8a-108">**Ввод**</span><span class="sxs-lookup"><span data-stu-id="9ee8a-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="9ee8a-109">[**\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) , содержащая идентификатор GUID для запроса и других данных.</span><span class="sxs-lookup"><span data-stu-id="9ee8a-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="9ee8a-110">**енкриптионгуидиндекс**</span><span class="sxs-lookup"><span data-stu-id="9ee8a-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="9ee8a-111">Индекс GUID шифрования.</span><span class="sxs-lookup"><span data-stu-id="9ee8a-111">The index of the encryption GUID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ee8a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9ee8a-112">Requirements</span></span>



| <span data-ttu-id="9ee8a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9ee8a-113">Requirement</span></span> | <span data-ttu-id="9ee8a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9ee8a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee8a-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ee8a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee8a-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9ee8a-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ee8a-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ee8a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee8a-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ee8a-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9ee8a-119">Header</span><span class="sxs-lookup"><span data-stu-id="9ee8a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ee8a-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ee8a-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee8a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ee8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee8a-122">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9ee8a-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="9ee8a-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9ee8a-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




