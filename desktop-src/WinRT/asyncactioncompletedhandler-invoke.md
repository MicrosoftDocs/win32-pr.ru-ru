---
description: Вызывает метод, вызываемый при завершении указанного асинхронного действия.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'Метод Асинкактионкомплетедхандлер:: Invoke'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145148"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a><span data-ttu-id="d9c22-103">Метод Асинкактионкомплетедхандлер:: Invoke</span><span class="sxs-lookup"><span data-stu-id="d9c22-103">AsyncActionCompletedHandler::Invoke method</span></span>

<span data-ttu-id="d9c22-104">Вызывает метод, вызываемый при завершении указанного асинхронного действия.</span><span class="sxs-lookup"><span data-stu-id="d9c22-104">Invokes the method that is called when the specified asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c22-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9c22-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d9c22-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9c22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9c22-107">*асинЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9c22-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c22-108">Тип: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _</span><span class="sxs-lookup"><span data-stu-id="d9c22-108">Type: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\** _</span></span>

<span data-ttu-id="d9c22-109">Асинхронное действие, которое сообщает о завершении.</span><span class="sxs-lookup"><span data-stu-id="d9c22-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9c22-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9c22-110">Return value</span></span>

<span data-ttu-id="d9c22-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d9c22-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d9c22-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d9c22-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9c22-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9c22-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c22-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d9c22-114">Requirements</span></span>



| <span data-ttu-id="d9c22-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d9c22-115">Requirement</span></span> | <span data-ttu-id="d9c22-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d9c22-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c22-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9c22-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d9c22-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d9c22-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="d9c22-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9c22-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d9c22-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9c22-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="d9c22-121">Header</span><span class="sxs-lookup"><span data-stu-id="d9c22-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9c22-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d9c22-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9c22-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9c22-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c22-124">**асинкактионкомплетедхандлер**</span><span class="sxs-lookup"><span data-stu-id="d9c22-124">**AsyncActionCompletedHandler**</span></span>](asyncactioncompletedhandler.md)
</dt> </dl>

 

