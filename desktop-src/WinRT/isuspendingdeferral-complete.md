---
description: Уведомляет систему, что приложение сохранило свои данные и готово к приостановке.
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'Метод Исуспендингдеферрал:: Complete (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711057"
---
# <a name="isuspendingdeferralcomplete-method"></a><span data-ttu-id="bc267-103">Метод Исуспендингдеферрал:: Complete</span><span class="sxs-lookup"><span data-stu-id="bc267-103">ISuspendingDeferral::Complete method</span></span>

<span data-ttu-id="bc267-104">Уведомляет систему, что приложение сохранило свои данные и готово к приостановке.</span><span class="sxs-lookup"><span data-stu-id="bc267-104">Notifies the system that the app has saved its data and is ready to be suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc267-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc267-105">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="bc267-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc267-106">Parameters</span></span>

<span data-ttu-id="bc267-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bc267-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc267-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc267-108">Return value</span></span>

<span data-ttu-id="bc267-109">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="bc267-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc267-110">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc267-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc267-111">Требования</span><span class="sxs-lookup"><span data-stu-id="bc267-111">Requirements</span></span>



| <span data-ttu-id="bc267-112">Требование</span><span class="sxs-lookup"><span data-stu-id="bc267-112">Requirement</span></span> | <span data-ttu-id="bc267-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bc267-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc267-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc267-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bc267-115">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bc267-115">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bc267-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc267-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bc267-117">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc267-117">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bc267-118">Header</span><span class="sxs-lookup"><span data-stu-id="bc267-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc267-119"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc267-119"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc267-120">IDL</span><span class="sxs-lookup"><span data-stu-id="bc267-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc267-121"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc267-121"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc267-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc267-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc267-123">**исуспендингдеферрал**</span><span class="sxs-lookup"><span data-stu-id="bc267-123">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 




