---
description: 'Содержит ответ от метода IDirect3DAuthenticatedChannel9:: Query.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: Структура D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143180"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a><span data-ttu-id="5a0e7-103">\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="5a0e7-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT structure</span></span>

<span data-ttu-id="5a0e7-104">Содержит ответ от метода [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="5a0e7-104">Contains the response from the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a0e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a0e7-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="5a0e7-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5a0e7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a0e7-107">**омак**</span><span class="sxs-lookup"><span data-stu-id="5a0e7-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="5a0e7-108">Структура [**D3D \_ ОМАК**](d3d-omac.md) , содержащая код проверки подлинности сообщения (Mac) данных.</span><span class="sxs-lookup"><span data-stu-id="5a0e7-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="5a0e7-109">Для вычисления этого значения в блоке данных, который отображается после этого элемента структуры, драйвер использует одноключовый CBC MAC (ОМАК) на основе AES.</span><span class="sxs-lookup"><span data-stu-id="5a0e7-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="5a0e7-110">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="5a0e7-110">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="5a0e7-111">Идентификатор GUID, указывающий запрос.</span><span class="sxs-lookup"><span data-stu-id="5a0e7-111">A GUID that specifies the query.</span></span> <span data-ttu-id="5a0e7-112">Список значений см. в разделе [запросы защита содержимого](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="5a0e7-112">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a0e7-113">**СПРАВИТЬСЯ**</span><span class="sxs-lookup"><span data-stu-id="5a0e7-113">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="5a0e7-114">Маркер для аутентифицированного канала.</span><span class="sxs-lookup"><span data-stu-id="5a0e7-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="5a0e7-115">**UINT**</span><span class="sxs-lookup"><span data-stu-id="5a0e7-115">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="5a0e7-116">Порядковый номер запроса.</span><span class="sxs-lookup"><span data-stu-id="5a0e7-116">The query sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="5a0e7-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="5a0e7-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="5a0e7-118">Код результата для запроса.</span><span class="sxs-lookup"><span data-stu-id="5a0e7-118">The result code for the query.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a0e7-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a0e7-119">Remarks</span></span>

<span data-ttu-id="5a0e7-120">Для членов **QueryType**, **хчаннел** и **SequenceNumber** драйвер использует те же значения, что и приложение, предоставленное в структуре [**\_ \_ входных данных запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) .</span><span class="sxs-lookup"><span data-stu-id="5a0e7-120">For the **QueryType**, **hChannel**, and **SequenceNumber** members, the driver uses in the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure.</span></span> <span data-ttu-id="5a0e7-121">Приложение должно проверить, совпадают ли эти значения.</span><span class="sxs-lookup"><span data-stu-id="5a0e7-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0e7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5a0e7-122">Requirements</span></span>



| <span data-ttu-id="5a0e7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5a0e7-123">Requirement</span></span> | <span data-ttu-id="5a0e7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5a0e7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0e7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a0e7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a0e7-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5a0e7-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5a0e7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a0e7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a0e7-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a0e7-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5a0e7-129">Header</span><span class="sxs-lookup"><span data-stu-id="5a0e7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a0e7-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a0e7-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a0e7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a0e7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0e7-132">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="5a0e7-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="5a0e7-133">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="5a0e7-133">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




