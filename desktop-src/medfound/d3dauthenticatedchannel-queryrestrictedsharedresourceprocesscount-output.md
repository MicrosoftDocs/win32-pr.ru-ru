---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY рестриктедшаредресаурцепроцесскаунт.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808135"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a><span data-ttu-id="30aa3-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесскаунт</span><span class="sxs-lookup"><span data-stu-id="30aa3-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="30aa3-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесскаунт**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .</span><span class="sxs-lookup"><span data-stu-id="30aa3-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) query.</span></span>

<span data-ttu-id="30aa3-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="30aa3-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="30aa3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30aa3-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="30aa3-107">Члены</span><span class="sxs-lookup"><span data-stu-id="30aa3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="30aa3-108">**Выходные данные**</span><span class="sxs-lookup"><span data-stu-id="30aa3-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="30aa3-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="30aa3-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="30aa3-110">**нумрестриктедшаредресаурцепроцессес**</span><span class="sxs-lookup"><span data-stu-id="30aa3-110">**NumRestrictedSharedResourceProcesses**</span></span>
</dt> <dd>

<span data-ttu-id="30aa3-111">Количество процессов, которым разрешено открывать общие ресурсы с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="30aa3-111">The number of processes allowed to open shared resources that have restricted access.</span></span> <span data-ttu-id="30aa3-112">Процесс не может открыть такой ресурс, если этому процессу не предоставлен доступ.</span><span class="sxs-lookup"><span data-stu-id="30aa3-112">A process cannot open such a resource unless the process has been granted access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30aa3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="30aa3-113">Requirements</span></span>



| <span data-ttu-id="30aa3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="30aa3-114">Requirement</span></span> | <span data-ttu-id="30aa3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="30aa3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30aa3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30aa3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="30aa3-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="30aa3-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30aa3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30aa3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="30aa3-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="30aa3-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="30aa3-120">Header</span><span class="sxs-lookup"><span data-stu-id="30aa3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="30aa3-121"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="30aa3-121"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30aa3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30aa3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30aa3-123">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="30aa3-123">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="30aa3-124">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="30aa3-124">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




