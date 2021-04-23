---
description: Изменения, которые монитор используется для закрепленных панелей инструментов в системе с несколькими мониторами.
title: 'Метод Имултимонитордоккингсите:: Сетмонитор'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997967"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="efbb6-103">Метод Имултимонитордоккингсите:: Сетмонитор</span><span class="sxs-lookup"><span data-stu-id="efbb6-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="efbb6-104">Изменения, которые монитор используется для закрепленных панелей инструментов в системе с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="efbb6-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbb6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efbb6-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="efbb6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efbb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efbb6-107">*пунксрк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efbb6-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efbb6-108">Тип: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="efbb6-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="efbb6-109">Указатель на объект, реализующий интерфейс [_ *идоккингвиндов* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) , для которого изменяется монитор.</span><span class="sxs-lookup"><span data-stu-id="efbb6-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="efbb6-110">*хмоннев* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efbb6-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efbb6-111">Тип: **хмонитор**</span><span class="sxs-lookup"><span data-stu-id="efbb6-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="efbb6-112">Маркер монитора, который заменяет существующий монитор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efbb6-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="efbb6-113">*фмонолд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="efbb6-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efbb6-114">Тип: \**хмонитор \** _</span><span class="sxs-lookup"><span data-stu-id="efbb6-114">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="efbb6-115">При возврате этой функции содержит указатель на предыдущий обработчик монитора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efbb6-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efbb6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efbb6-116">Return value</span></span>

<span data-ttu-id="efbb6-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="efbb6-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="efbb6-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="efbb6-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="efbb6-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="efbb6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="efbb6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="efbb6-120">Requirements</span></span>



| <span data-ttu-id="efbb6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="efbb6-121">Requirement</span></span> | <span data-ttu-id="efbb6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="efbb6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="efbb6-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efbb6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="efbb6-124">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="efbb6-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="efbb6-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efbb6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="efbb6-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efbb6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
