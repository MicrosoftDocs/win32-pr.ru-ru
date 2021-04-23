---
description: Содержит входные данные для \_ запроса D3DAUTHENTICATEDQUERY рестриктедшаредресаурцепроцесс.
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 06c4421f048af80186077da022fdecfaea79dca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673156"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a><span data-ttu-id="4f662-103">\_ \_ Входная структура D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесс</span><span class="sxs-lookup"><span data-stu-id="4f662-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT structure</span></span>

<span data-ttu-id="4f662-104">Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесс**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .</span><span class="sxs-lookup"><span data-stu-id="4f662-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="4f662-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="4f662-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f662-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f662-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                ProcessIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT;
```



## <a name="members"></a><span data-ttu-id="4f662-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4f662-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f662-108">**Ввод**</span><span class="sxs-lookup"><span data-stu-id="4f662-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="4f662-109">[**\_ \_ Входная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) , содержащая идентификатор GUID для запроса и других данных.</span><span class="sxs-lookup"><span data-stu-id="4f662-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="4f662-110">**процессиндекс**</span><span class="sxs-lookup"><span data-stu-id="4f662-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4f662-111">Индекс процесса.</span><span class="sxs-lookup"><span data-stu-id="4f662-111">The index of the process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f662-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4f662-112">Requirements</span></span>



| <span data-ttu-id="4f662-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4f662-113">Requirement</span></span> | <span data-ttu-id="4f662-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4f662-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f662-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f662-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4f662-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4f662-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4f662-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f662-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4f662-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f662-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4f662-119">Header</span><span class="sxs-lookup"><span data-stu-id="4f662-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f662-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f662-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f662-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f662-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f662-122">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="4f662-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4f662-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="4f662-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




