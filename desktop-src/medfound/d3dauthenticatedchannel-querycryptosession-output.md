---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY CRYPTOSESSION.
ms.assetid: df9d9b41-8188-4597-9e83-d14065eb7fc7
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fb4e6ccad999f183e71f0f57d64544a70cef5534
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692059"
---
# <a name="d3dauthenticatedchannel_querycryptosession_output-structure"></a><span data-ttu-id="a5b6d-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куерикриптосессион</span><span class="sxs-lookup"><span data-stu-id="a5b6d-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT structure</span></span>

<span data-ttu-id="a5b6d-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b6d-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="a5b6d-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="a5b6d-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b6d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5b6d-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DXVA2DecodeHandle;
  HANDLE                               CryptoSessionHandle;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="a5b6d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a5b6d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5b6d-108">**Выходные данные**</span><span class="sxs-lookup"><span data-stu-id="a5b6d-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="a5b6d-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="a5b6d-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="a5b6d-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a5b6d-111">Маркер устройства декодера DirectX Video Acceleration 2 (ДКСВА-2).</span><span class="sxs-lookup"><span data-stu-id="a5b6d-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="a5b6d-112">**криптосессионхандле**</span><span class="sxs-lookup"><span data-stu-id="a5b6d-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a5b6d-113">Обработчик сеанса шифрования, связанный с устройством декодера.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-113">A handle to the cryptographic session that is associated with the decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="a5b6d-114">**девицехандле**</span><span class="sxs-lookup"><span data-stu-id="a5b6d-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a5b6d-115">Маркер устройства Direct3D, связанного с устройством декодера.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-115">A handle to the Direct3D device that is associated with the decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5b6d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a5b6d-116">Requirements</span></span>



| <span data-ttu-id="a5b6d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a5b6d-117">Requirement</span></span> | <span data-ttu-id="a5b6d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a5b6d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b6d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5b6d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b6d-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a5b6d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a5b6d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5b6d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b6d-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5b6d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a5b6d-123">Header</span><span class="sxs-lookup"><span data-stu-id="a5b6d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b6d-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b6d-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b6d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5b6d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b6d-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="a5b6d-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a5b6d-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a5b6d-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




