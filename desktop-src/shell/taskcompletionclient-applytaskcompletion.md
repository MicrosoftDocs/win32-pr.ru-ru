---
description: Начинает выполнение задачи.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'Метод Тасккомплетионклиент:: Апплитасккомплетион'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997850"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a><span data-ttu-id="b7f21-103">Метод Тасккомплетионклиент:: Апплитасккомплетион</span><span class="sxs-lookup"><span data-stu-id="b7f21-103">TaskCompletionClient::ApplyTaskCompletion method</span></span>

<span data-ttu-id="b7f21-104">Начинает выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="b7f21-104">Begins the task completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f21-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7f21-105">Syntax</span></span>


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a><span data-ttu-id="b7f21-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7f21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7f21-107">*пткфкатегори*</span><span class="sxs-lookup"><span data-stu-id="b7f21-107">*ptcfCategory*</span></span> 
</dt> <dd>

<span data-ttu-id="b7f21-108">Значение, указывающее категорию задачи.</span><span class="sxs-lookup"><span data-stu-id="b7f21-108">A value indicating the category of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7f21-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7f21-109">Return value</span></span>

<span data-ttu-id="b7f21-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b7f21-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7f21-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7f21-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7f21-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7f21-112">Remarks</span></span>

<span data-ttu-id="b7f21-113">Единственным поддерживаемым значением для *пткфкатегори* является 0x08000000.</span><span class="sxs-lookup"><span data-stu-id="b7f21-113">The only supported value for *ptcfCategory* is 0x08000000.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f21-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b7f21-114">Requirements</span></span>



| <span data-ttu-id="b7f21-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b7f21-115">Requirement</span></span> | <span data-ttu-id="b7f21-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f21-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f21-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7f21-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f21-118">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b7f21-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7f21-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7f21-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f21-120">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="b7f21-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7f21-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b7f21-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f21-122"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7f21-122"><dt>ExecModelClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f21-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7f21-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f21-124">**тасккомплетионклиент**</span><span class="sxs-lookup"><span data-stu-id="b7f21-124">**TaskCompletionClient**</span></span>](taskcompletionclient.md)
</dt> </dl>

 

 




