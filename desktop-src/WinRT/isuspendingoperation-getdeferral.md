---
description: Запрашивает задержку операции приостановки выполнения приложения.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'Метод Исуспендингоператион:: откладывания (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897378"
---
# <a name="isuspendingoperationgetdeferral-method"></a><span data-ttu-id="88e3b-103">Метод Исуспендингоператион:: откладывания</span><span class="sxs-lookup"><span data-stu-id="88e3b-103">ISuspendingOperation::GetDeferral method</span></span>

<span data-ttu-id="88e3b-104">Запрашивает задержку операции приостановки выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="88e3b-104">Requests that the app suspending operation be delayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e3b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88e3b-105">Syntax</span></span>


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a><span data-ttu-id="88e3b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88e3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88e3b-107">*РБП* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="88e3b-107">*deferral* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="88e3b-108">Приостановка отсрочки.</span><span class="sxs-lookup"><span data-stu-id="88e3b-108">The deferral suspension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88e3b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88e3b-109">Return value</span></span>

<span data-ttu-id="88e3b-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="88e3b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88e3b-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88e3b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e3b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="88e3b-112">Requirements</span></span>



| <span data-ttu-id="88e3b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="88e3b-113">Requirement</span></span> | <span data-ttu-id="88e3b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="88e3b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e3b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88e3b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="88e3b-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="88e3b-116">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="88e3b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88e3b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="88e3b-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88e3b-118">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="88e3b-119">Header</span><span class="sxs-lookup"><span data-stu-id="88e3b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="88e3b-120"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="88e3b-120"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="88e3b-121">IDL</span><span class="sxs-lookup"><span data-stu-id="88e3b-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88e3b-122"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88e3b-122"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e3b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88e3b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e3b-124">**исуспендингоператион**</span><span class="sxs-lookup"><span data-stu-id="88e3b-124">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




