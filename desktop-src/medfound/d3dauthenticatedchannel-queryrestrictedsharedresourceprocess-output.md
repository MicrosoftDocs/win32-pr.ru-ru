---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY рестриктедшаредресаурцепроцесс.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143165"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a><span data-ttu-id="a310a-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесс</span><span class="sxs-lookup"><span data-stu-id="a310a-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT structure</span></span>

<span data-ttu-id="a310a-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесс**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .</span><span class="sxs-lookup"><span data-stu-id="a310a-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="a310a-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="a310a-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="a310a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a310a-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="a310a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a310a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a310a-108">**Выходные данные**</span><span class="sxs-lookup"><span data-stu-id="a310a-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="a310a-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="a310a-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="a310a-110">**процессиндекс**</span><span class="sxs-lookup"><span data-stu-id="a310a-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a310a-111">Индекс процесса в списке процессов.</span><span class="sxs-lookup"><span data-stu-id="a310a-111">The index of the process in the list of processes.</span></span>

</dd> <dt>

<span data-ttu-id="a310a-112">**процессидентифер**</span><span class="sxs-lookup"><span data-stu-id="a310a-112">**ProcessIdentifer**</span></span>
</dt> <dd>

<span data-ttu-id="a310a-113">Значение [**D3DAUTHENTICATEDCHANNEL \_ процессидентифиертипе**](d3dauthenticatedchannel-processidentifiertype.md) , указывающее тип процесса.</span><span class="sxs-lookup"><span data-stu-id="a310a-113">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span>

</dd> <dt>

<span data-ttu-id="a310a-114">**процесшандле**</span><span class="sxs-lookup"><span data-stu-id="a310a-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a310a-115">Обработчик процесса.</span><span class="sxs-lookup"><span data-stu-id="a310a-115">A process handle.</span></span> <span data-ttu-id="a310a-116">Если элемент **процессидентифиер** равен **процессидтипе \_ Handle**, то элемент **процесшандле** содержит допустимый обработчик для процесса.</span><span class="sxs-lookup"><span data-stu-id="a310a-116">If the **ProcessIdentifier** member equals **PROCESSIDTYPE\_HANDLE**, the **ProcessHandle** member contains a valid handle to a process.</span></span> <span data-ttu-id="a310a-117">В противном случае этот элемент игнорируется.</span><span class="sxs-lookup"><span data-stu-id="a310a-117">Otherwise, this member is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a310a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a310a-118">Remarks</span></span>

<span data-ttu-id="a310a-119">Процесс диспетчер окон рабочего стола (DWM) определяется путем установки **процессидентифиер** равным **процессидтипе \_ DWM**.</span><span class="sxs-lookup"><span data-stu-id="a310a-119">The Desktop Window Manager (DWM) process is identified by setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="a310a-120">Другие процессы определяются путем установки обработчика процесса в **процесшандле** и установки **Процессидентифиер** равным **процессидтипе \_ Handle**.</span><span class="sxs-lookup"><span data-stu-id="a310a-120">Other processes are identified by setting the process handle in **ProcessHandle** and setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_HANDLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a310a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a310a-121">Requirements</span></span>



| <span data-ttu-id="a310a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a310a-122">Requirement</span></span> | <span data-ttu-id="a310a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a310a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a310a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a310a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a310a-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a310a-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a310a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a310a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a310a-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a310a-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a310a-128">Header</span><span class="sxs-lookup"><span data-stu-id="a310a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a310a-129"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a310a-129"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a310a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a310a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a310a-131">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="a310a-131">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a310a-132">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a310a-132">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




