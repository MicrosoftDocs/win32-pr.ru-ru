---
description: Возвращает метод, который вызывается после завершения асинхронного действия.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'Метод IAsyncAction:: get_Completed'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145136"
---
# <a name="iasyncactionget_completed-method"></a><span data-ttu-id="14f4f-103">Метод IAsyncAction:: Get \_ завершен</span><span class="sxs-lookup"><span data-stu-id="14f4f-103">IAsyncAction::get\_Completed method</span></span>

<span data-ttu-id="14f4f-104">Возвращает метод, который вызывается после завершения асинхронного действия.</span><span class="sxs-lookup"><span data-stu-id="14f4f-104">Gets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f4f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14f4f-105">Syntax</span></span>


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a><span data-ttu-id="14f4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14f4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14f4f-107">*обработчик событий* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="14f4f-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14f4f-108">Тип: **[ **асинкактионкомплетедхандлер**](asyncactioncompletedhandler.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="14f4f-108">Type: **[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span></span>

<span data-ttu-id="14f4f-109">Метод, обрабатывающий уведомление о завершении.</span><span class="sxs-lookup"><span data-stu-id="14f4f-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14f4f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14f4f-110">Return value</span></span>

<span data-ttu-id="14f4f-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14f4f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="14f4f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="14f4f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14f4f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14f4f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="14f4f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="14f4f-114">Requirements</span></span>



| <span data-ttu-id="14f4f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="14f4f-115">Requirement</span></span> | <span data-ttu-id="14f4f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="14f4f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f4f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14f4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14f4f-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14f4f-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="14f4f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14f4f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14f4f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14f4f-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="14f4f-121">Header</span><span class="sxs-lookup"><span data-stu-id="14f4f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14f4f-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14f4f-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14f4f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14f4f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f4f-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="14f4f-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
