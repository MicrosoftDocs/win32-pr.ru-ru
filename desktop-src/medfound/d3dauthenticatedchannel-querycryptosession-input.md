---
description: Содержит входные данные для \_ запроса D3DAUTHENTICATEDQUERY CRYPTOSESSION.
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 76b9d09bcb03dbf3742d551c253d3f4982215757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342525"
---
# <a name="d3dauthenticatedchannel_querycryptosession_input-structure"></a><span data-ttu-id="73f85-103">\_ \_ Входная структура D3DAUTHENTICATEDCHANNEL куерикриптосессион</span><span class="sxs-lookup"><span data-stu-id="73f85-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_INPUT structure</span></span>

<span data-ttu-id="73f85-104">Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="73f85-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="73f85-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="73f85-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="73f85-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73f85-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DXVA2DecodeHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT;
```



## <a name="members"></a><span data-ttu-id="73f85-107">Члены</span><span class="sxs-lookup"><span data-stu-id="73f85-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="73f85-108">**Ввод**</span><span class="sxs-lookup"><span data-stu-id="73f85-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="73f85-109">[**\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) , содержащая идентификатор GUID для запроса и других данных.</span><span class="sxs-lookup"><span data-stu-id="73f85-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="73f85-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="73f85-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="73f85-111">Маркер устройства декодера DirectX Video Acceleration 2 (ДКСВА-2).</span><span class="sxs-lookup"><span data-stu-id="73f85-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73f85-112">Требования</span><span class="sxs-lookup"><span data-stu-id="73f85-112">Requirements</span></span>



| <span data-ttu-id="73f85-113">Требование</span><span class="sxs-lookup"><span data-stu-id="73f85-113">Requirement</span></span> | <span data-ttu-id="73f85-114">Значение</span><span class="sxs-lookup"><span data-stu-id="73f85-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73f85-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73f85-115">Minimum supported client</span></span><br/> | <span data-ttu-id="73f85-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="73f85-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="73f85-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73f85-117">Minimum supported server</span></span><br/> | <span data-ttu-id="73f85-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="73f85-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="73f85-119">Header</span><span class="sxs-lookup"><span data-stu-id="73f85-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="73f85-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="73f85-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73f85-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73f85-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f85-122">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="73f85-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="73f85-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="73f85-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




