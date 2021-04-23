---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY унрестриктедпротектедшаредресаурцекаунт.
ms.assetid: c283833d-e98c-4f01-b623-21027a6b90e8
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fd30cff59d35f845903e7f4fdb08cdff61df3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673155"
---
# <a name="d3dauthenticatedchannel_queryunrestrictedprotectedsharedresourcecount_output-structure"></a><span data-ttu-id="19521-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куерюнрестриктедпротектедшаредресаурцекаунт</span><span class="sxs-lookup"><span data-stu-id="19521-103">D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="19521-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ унрестриктедпротектедшаредресаурцекаунт**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) .</span><span class="sxs-lookup"><span data-stu-id="19521-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) query.</span></span>

<span data-ttu-id="19521-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="19521-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="19521-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19521-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumUnrestrictedProtectedSharedResources;
} D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="19521-107">Члены</span><span class="sxs-lookup"><span data-stu-id="19521-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="19521-108">**Выходные данные**</span><span class="sxs-lookup"><span data-stu-id="19521-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="19521-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="19521-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="19521-110">**нумунрестриктедпротектедшаредресаурцес**</span><span class="sxs-lookup"><span data-stu-id="19521-110">**NumUnrestrictedProtectedSharedResources**</span></span>
</dt> <dd>

<span data-ttu-id="19521-111">Количество защищенных общих ресурсов, которые могут быть открыты любым процессом без ограничений.</span><span class="sxs-lookup"><span data-stu-id="19521-111">The number of protected, shared resources that can be opened by any process without restrictions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19521-112">Требования</span><span class="sxs-lookup"><span data-stu-id="19521-112">Requirements</span></span>



| <span data-ttu-id="19521-113">Требование</span><span class="sxs-lookup"><span data-stu-id="19521-113">Requirement</span></span> | <span data-ttu-id="19521-114">Значение</span><span class="sxs-lookup"><span data-stu-id="19521-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19521-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19521-115">Minimum supported client</span></span><br/> | <span data-ttu-id="19521-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="19521-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="19521-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19521-117">Minimum supported server</span></span><br/> | <span data-ttu-id="19521-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="19521-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="19521-119">Header</span><span class="sxs-lookup"><span data-stu-id="19521-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="19521-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="19521-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19521-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19521-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19521-122">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="19521-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="19521-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="19521-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




