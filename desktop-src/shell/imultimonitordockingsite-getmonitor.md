---
description: Возвращает текущий монитор по умолчанию.
title: 'Метод Имултимонитордоккингсите::'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840645"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="57965-103">Метод Имултимонитордоккингсите::</span><span class="sxs-lookup"><span data-stu-id="57965-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="57965-104">Возвращает текущий монитор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57965-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="57965-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57965-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="57965-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57965-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57965-107">*пунксрк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57965-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57965-108">Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="57965-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="57965-109">Указатель на объект, реализующий интерфейс [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) , для которого запрашивается монитор.</span><span class="sxs-lookup"><span data-stu-id="57965-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="57965-110">*фмон* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="57965-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57965-111">Тип: **хмонитор \***</span><span class="sxs-lookup"><span data-stu-id="57965-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="57965-112">При возврате функции содержит указатель на обработчик монитора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57965-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57965-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57965-113">Return value</span></span>

<span data-ttu-id="57965-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="57965-114">Type: **HRESULT**</span></span>

<span data-ttu-id="57965-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="57965-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57965-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57965-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="57965-117">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="57965-117">Requirements</span></span>



| <span data-ttu-id="57965-118">Требование</span><span class="sxs-lookup"><span data-stu-id="57965-118">Requirement</span></span> | <span data-ttu-id="57965-119">Значение</span><span class="sxs-lookup"><span data-stu-id="57965-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="57965-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57965-120">Minimum supported client</span></span><br/> | <span data-ttu-id="57965-121">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="57965-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="57965-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57965-122">Minimum supported server</span></span><br/> | <span data-ttu-id="57965-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="57965-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
