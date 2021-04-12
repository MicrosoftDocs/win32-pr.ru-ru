---
description: Возвращает результат асинхронного действия.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'IAsyncAction:: Results, метод'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263086"
---
# <a name="iasyncactiongetresults-method"></a><span data-ttu-id="4765d-103">IAsyncAction:: Results, метод</span><span class="sxs-lookup"><span data-stu-id="4765d-103">IAsyncAction::GetResults method</span></span>

<span data-ttu-id="4765d-104">Возвращает результат асинхронного действия.</span><span class="sxs-lookup"><span data-stu-id="4765d-104">Gets the outcome of an asynchronous action.</span></span>

## <a name="syntax"></a><span data-ttu-id="4765d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4765d-105">Syntax</span></span>


```C++
HRESULT GetResults();
```



## <a name="parameters"></a><span data-ttu-id="4765d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4765d-106">Parameters</span></span>

<span data-ttu-id="4765d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4765d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4765d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4765d-108">Return value</span></span>

<span data-ttu-id="4765d-109">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4765d-109">Type: **HRESULT**</span></span>

<span data-ttu-id="4765d-110">Этот метод всегда возвращает значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4765d-110">This method always returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4765d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4765d-111">Remarks</span></span>

<span data-ttu-id="4765d-112">Вызов метода **IAsyncAction** не имеет силы, если текущая реализация имеет динамический тип [](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span><span class="sxs-lookup"><span data-stu-id="4765d-112">Calling the **GetResults** method has no effect if the current implementation has a dynamic type of [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span></span>

## <a name="requirements"></a><span data-ttu-id="4765d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4765d-113">Requirements</span></span>



| <span data-ttu-id="4765d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4765d-114">Requirement</span></span> | <span data-ttu-id="4765d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4765d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4765d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4765d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4765d-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4765d-117">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="4765d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4765d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4765d-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4765d-119">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="4765d-120">Header</span><span class="sxs-lookup"><span data-stu-id="4765d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4765d-121"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4765d-121"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4765d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4765d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4765d-123">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="4765d-123">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
