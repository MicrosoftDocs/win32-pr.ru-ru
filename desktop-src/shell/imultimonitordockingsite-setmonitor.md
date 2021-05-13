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
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841945"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="6ddfc-103">Метод Имултимонитордоккингсите:: Сетмонитор</span><span class="sxs-lookup"><span data-stu-id="6ddfc-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="6ddfc-104">Изменения, которые монитор используется для закрепленных панелей инструментов в системе с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ddfc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ddfc-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="6ddfc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ddfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ddfc-107">*пунксрк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ddfc-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ddfc-108">Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="6ddfc-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="6ddfc-109">Указатель на объект, реализующий интерфейс [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) , для которого изменяется монитор.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="6ddfc-110">*хмоннев* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ddfc-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ddfc-111">Тип: **хмонитор**</span><span class="sxs-lookup"><span data-stu-id="6ddfc-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="6ddfc-112">Маркер монитора, который заменяет существующий монитор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6ddfc-113">*фмонолд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6ddfc-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ddfc-114">Тип: **хмонитор \***</span><span class="sxs-lookup"><span data-stu-id="6ddfc-114">Type: **HMONITOR\***</span></span>

<span data-ttu-id="6ddfc-115">При возврате этой функции содержит указатель на предыдущий обработчик монитора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ddfc-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ddfc-116">Return value</span></span>

<span data-ttu-id="6ddfc-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6ddfc-117">Type: **HRESULT**</span></span>

<span data-ttu-id="6ddfc-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ddfc-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ddfc-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ddfc-120">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="6ddfc-120">Requirements</span></span>



| <span data-ttu-id="6ddfc-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6ddfc-121">Requirement</span></span> | <span data-ttu-id="6ddfc-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6ddfc-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6ddfc-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ddfc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6ddfc-124">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ddfc-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6ddfc-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ddfc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6ddfc-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ddfc-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
