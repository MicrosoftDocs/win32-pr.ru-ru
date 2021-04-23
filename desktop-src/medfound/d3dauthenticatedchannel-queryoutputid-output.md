---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY аутпутид.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072573"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a><span data-ttu-id="30814-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куерираутпутид</span><span class="sxs-lookup"><span data-stu-id="30814-103">D3DAUTHENTICATEDCHANNEL\_QUERYROUTPUTID\_OUTPUT structure</span></span>

<span data-ttu-id="30814-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ аутпутид**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="30814-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="30814-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="30814-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="30814-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30814-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="30814-107">Члены</span><span class="sxs-lookup"><span data-stu-id="30814-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="30814-108">**\_ \_ Выходные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="30814-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="30814-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="30814-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="30814-110">**девицехандле**</span><span class="sxs-lookup"><span data-stu-id="30814-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="30814-111">Маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="30814-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="30814-112">**криптосессионхандле**</span><span class="sxs-lookup"><span data-stu-id="30814-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="30814-113">Маркер сеанса шифрования.</span><span class="sxs-lookup"><span data-stu-id="30814-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="30814-114">**аутпутидиндекс**</span><span class="sxs-lookup"><span data-stu-id="30814-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="30814-115">Индекс выходного идентификатора, заданного в элементе **аутпутид** .</span><span class="sxs-lookup"><span data-stu-id="30814-115">The index of the output ID given in the **OutputID** member.</span></span>

</dd> <dt>

<span data-ttu-id="30814-116">**аутпутид**</span><span class="sxs-lookup"><span data-stu-id="30814-116">**OutputID**</span></span>
</dt> <dd>

<span data-ttu-id="30814-117">Идентификатор выхода, связанный с указанным устройством и сеансом шифрования.</span><span class="sxs-lookup"><span data-stu-id="30814-117">An output ID that is associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30814-118">Требования</span><span class="sxs-lookup"><span data-stu-id="30814-118">Requirements</span></span>



| <span data-ttu-id="30814-119">Требование</span><span class="sxs-lookup"><span data-stu-id="30814-119">Requirement</span></span> | <span data-ttu-id="30814-120">Значение</span><span class="sxs-lookup"><span data-stu-id="30814-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30814-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30814-121">Minimum supported client</span></span><br/> | <span data-ttu-id="30814-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="30814-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30814-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30814-123">Minimum supported server</span></span><br/> | <span data-ttu-id="30814-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="30814-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="30814-125">Header</span><span class="sxs-lookup"><span data-stu-id="30814-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="30814-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="30814-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30814-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30814-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30814-128">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="30814-128">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="30814-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="30814-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




