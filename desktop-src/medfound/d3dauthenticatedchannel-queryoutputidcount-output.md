---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY аутпутидкаунт.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 86a840de2b36b7089b31d15e8375c17a0610b77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496821"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a><span data-ttu-id="3e085-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куерйоутпутидкаунт</span><span class="sxs-lookup"><span data-stu-id="3e085-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="3e085-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="3e085-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="3e085-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="3e085-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e085-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e085-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="3e085-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3e085-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e085-108">**Выходные данные**</span><span class="sxs-lookup"><span data-stu-id="3e085-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="3e085-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="3e085-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="3e085-110">**девицехандле**</span><span class="sxs-lookup"><span data-stu-id="3e085-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="3e085-111">Маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="3e085-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="3e085-112">**криптосессионхандле**</span><span class="sxs-lookup"><span data-stu-id="3e085-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="3e085-113">Маркер сеанса шифрования.</span><span class="sxs-lookup"><span data-stu-id="3e085-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="3e085-114">**нумаутпутидс**</span><span class="sxs-lookup"><span data-stu-id="3e085-114">**NumOutputIDs**</span></span>
</dt> <dd>

<span data-ttu-id="3e085-115">Число идентификаторов выходных данных, связанных с указанным устройством и сеансом шифрования.</span><span class="sxs-lookup"><span data-stu-id="3e085-115">The number of output IDs associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e085-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3e085-116">Requirements</span></span>



| <span data-ttu-id="3e085-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3e085-117">Requirement</span></span> | <span data-ttu-id="3e085-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3e085-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e085-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e085-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e085-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e085-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3e085-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e085-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e085-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e085-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3e085-123">Header</span><span class="sxs-lookup"><span data-stu-id="3e085-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e085-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e085-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e085-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e085-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e085-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="3e085-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="3e085-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="3e085-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




