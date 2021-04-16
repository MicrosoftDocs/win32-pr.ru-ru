---
description: Содержит входные данные для \_ запроса D3DAUTHENTICATEDQUERY аутпутид.
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7c64d43261ccc849772372110ad73169c698cd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719273"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a><span data-ttu-id="111d6-103">\_ \_ Входная структура D3DAUTHENTICATEDCHANNEL куерйоутпутид</span><span class="sxs-lookup"><span data-stu-id="111d6-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT structure</span></span>

<span data-ttu-id="111d6-104">Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ аутпутид**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="111d6-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="111d6-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="111d6-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="111d6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="111d6-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a><span data-ttu-id="111d6-107">Члены</span><span class="sxs-lookup"><span data-stu-id="111d6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="111d6-108">**Ввод**</span><span class="sxs-lookup"><span data-stu-id="111d6-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="111d6-109">[**\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) , содержащая идентификатор GUID для запроса и других данных.</span><span class="sxs-lookup"><span data-stu-id="111d6-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="111d6-110">**девицехандле**</span><span class="sxs-lookup"><span data-stu-id="111d6-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="111d6-111">Маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="111d6-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="111d6-112">**криптосессионхандле**</span><span class="sxs-lookup"><span data-stu-id="111d6-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="111d6-113">Маркер сеанса шифрования.</span><span class="sxs-lookup"><span data-stu-id="111d6-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="111d6-114">**аутпутидиндекс**</span><span class="sxs-lookup"><span data-stu-id="111d6-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="111d6-115">Индекс выходного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="111d6-115">The index of the output ID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="111d6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="111d6-116">Requirements</span></span>



| <span data-ttu-id="111d6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="111d6-117">Requirement</span></span> | <span data-ttu-id="111d6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="111d6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="111d6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="111d6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="111d6-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="111d6-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="111d6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="111d6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="111d6-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="111d6-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="111d6-123">Header</span><span class="sxs-lookup"><span data-stu-id="111d6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="111d6-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="111d6-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="111d6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="111d6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111d6-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="111d6-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="111d6-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="111d6-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




