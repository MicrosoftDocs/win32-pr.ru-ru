---
description: Задает метод, который вызывается при завершении асинхронного действия.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: 'IAsyncAction: метод ut_Completed:p'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991124"
---
# <a name="iasyncactionput_completed-method"></a><span data-ttu-id="52885-103">IAsyncAction: метод:p UT \_ завершен</span><span class="sxs-lookup"><span data-stu-id="52885-103">IAsyncAction::put\_Completed method</span></span>

<span data-ttu-id="52885-104">Задает метод, который вызывается при завершении асинхронного действия.</span><span class="sxs-lookup"><span data-stu-id="52885-104">Sets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="52885-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52885-105">Syntax</span></span>


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a><span data-ttu-id="52885-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="52885-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52885-107">*обработчик событий* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="52885-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52885-108">Тип: \**[**асинкактионкомплетедхандлер**](asyncactioncompletedhandler.md) \** _</span><span class="sxs-lookup"><span data-stu-id="52885-108">Type: \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\** _</span></span>

<span data-ttu-id="52885-109">Метод, обрабатывающий уведомление о завершении.</span><span class="sxs-lookup"><span data-stu-id="52885-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52885-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52885-110">Return value</span></span>

<span data-ttu-id="52885-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="52885-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="52885-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="52885-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52885-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="52885-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="52885-114">Требования</span><span class="sxs-lookup"><span data-stu-id="52885-114">Requirements</span></span>



| <span data-ttu-id="52885-115">Требование</span><span class="sxs-lookup"><span data-stu-id="52885-115">Requirement</span></span> | <span data-ttu-id="52885-116">Значение</span><span class="sxs-lookup"><span data-stu-id="52885-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52885-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52885-117">Minimum supported client</span></span><br/> | <span data-ttu-id="52885-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52885-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="52885-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52885-119">Minimum supported server</span></span><br/> | <span data-ttu-id="52885-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52885-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="52885-121">Header</span><span class="sxs-lookup"><span data-stu-id="52885-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="52885-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52885-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52885-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52885-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52885-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="52885-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
