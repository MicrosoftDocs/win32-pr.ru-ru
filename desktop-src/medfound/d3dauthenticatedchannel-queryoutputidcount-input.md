---
description: Содержит входные данные для \_ запроса D3DAUTHENTICATEDQUERY аутпутидкаунт.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 93f58bcd05efb8c173986186d631c713195d8363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143174"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a><span data-ttu-id="a2eab-103">\_ \_ Входная структура D3DAUTHENTICATEDCHANNEL куерйоутпутидкаунт</span><span class="sxs-lookup"><span data-stu-id="a2eab-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT structure</span></span>

<span data-ttu-id="a2eab-104">Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="a2eab-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="a2eab-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="a2eab-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2eab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2eab-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a><span data-ttu-id="a2eab-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a2eab-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2eab-108">**Ввод**</span><span class="sxs-lookup"><span data-stu-id="a2eab-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="a2eab-109">[**\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) , содержащая идентификатор GUID для запроса и других данных.</span><span class="sxs-lookup"><span data-stu-id="a2eab-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="a2eab-110">**девицехандле**</span><span class="sxs-lookup"><span data-stu-id="a2eab-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a2eab-111">Маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="a2eab-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="a2eab-112">**криптосессионхандле**</span><span class="sxs-lookup"><span data-stu-id="a2eab-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a2eab-113">Маркер сеанса шифрования.</span><span class="sxs-lookup"><span data-stu-id="a2eab-113">A handle to the cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2eab-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a2eab-114">Requirements</span></span>



| <span data-ttu-id="a2eab-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a2eab-115">Requirement</span></span> | <span data-ttu-id="a2eab-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a2eab-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2eab-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2eab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2eab-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a2eab-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2eab-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2eab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2eab-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2eab-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a2eab-121">Header</span><span class="sxs-lookup"><span data-stu-id="a2eab-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2eab-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2eab-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2eab-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2eab-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2eab-124">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="a2eab-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a2eab-125">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a2eab-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




