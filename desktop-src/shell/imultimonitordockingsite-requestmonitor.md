---
description: Проверяет, что монитор активен и доступен.
title: 'Метод Имултимонитордоккингсите:: Рекуестмонитор'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 5389b10af9aaa3da5d3106d82a4fbdcbd614a094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999705"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="8a068-103">Метод Имултимонитордоккингсите:: Рекуестмонитор</span><span class="sxs-lookup"><span data-stu-id="8a068-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="8a068-104">Проверяет, что монитор активен и доступен.</span><span class="sxs-lookup"><span data-stu-id="8a068-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a068-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a068-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="8a068-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a068-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a068-107">*пунксрк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a068-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a068-108">Тип: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="8a068-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="8a068-109">Указатель на объект, реализующий интерфейс [_ *идоккингвиндов* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) .</span><span class="sxs-lookup"><span data-stu-id="8a068-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8a068-110">*фмон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a068-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a068-111">Тип: \**хмонитор \** _</span><span class="sxs-lookup"><span data-stu-id="8a068-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="8a068-112">Указатель на обработчик монитора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a068-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a068-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a068-113">Return value</span></span>

<span data-ttu-id="8a068-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8a068-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8a068-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8a068-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a068-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a068-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a068-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8a068-117">Requirements</span></span>



| <span data-ttu-id="8a068-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8a068-118">Requirement</span></span> | <span data-ttu-id="8a068-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8a068-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="8a068-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a068-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8a068-121">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8a068-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8a068-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a068-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8a068-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a068-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
