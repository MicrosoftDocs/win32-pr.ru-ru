---
title: Имстскаксевентс Онрекуестлеавефуллскрин, метод
description: Вызывается, когда клиент запрашивает, чтобы выйти из полноэкранного режима, а свойству Имстскадванцедсеттингс помещается \_ контаинерхандледфуллскрин присвоено ненулевое значение.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онрекуестлеавефуллскрин
- Службы удаленных рабочих столов метода Онрекуестлеавефуллскрин, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онрекуестлеавефуллскрин
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802722"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a><span data-ttu-id="3c0d8-106">Метод Имстскаксевентс:: Онрекуестлеавефуллскрин</span><span class="sxs-lookup"><span data-stu-id="3c0d8-106">IMsTscAxEvents::OnRequestLeaveFullScreen method</span></span>

<span data-ttu-id="3c0d8-107">Вызывается, когда клиент запрашивает, чтобы выйти из полноэкранного режима, а свойство [**имстскадванцедсеттингс::p UT \_ контаинерхандледфуллскрин**](imstscadvancedsettings-containerhandledfullscreen.md) установлено в ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-107">Called when the client requests to leave full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) property has been set to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0d8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c0d8-108">Syntax</span></span>


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="3c0d8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c0d8-109">Parameters</span></span>

<span data-ttu-id="3c0d8-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c0d8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c0d8-111">Return value</span></span>

<span data-ttu-id="3c0d8-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c0d8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c0d8-113">Remarks</span></span>

<span data-ttu-id="3c0d8-114">В полноэкранном режиме, поддерживающем контейнеры, контейнер должен оставить стандартный полноэкранный режим в ответ на это событие.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-114">In container-handled full-screen mode, the container should leave standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="3c0d8-115">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3c0d8-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0d8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3c0d8-116">Requirements</span></span>



| <span data-ttu-id="3c0d8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3c0d8-117">Requirement</span></span> | <span data-ttu-id="3c0d8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3c0d8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0d8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c0d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0d8-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c0d8-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3c0d8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c0d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0d8-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c0d8-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3c0d8-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3c0d8-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c0d8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c0d8-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3c0d8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3c0d8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c0d8-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c0d8-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3c0d8-127">IID</span><span class="sxs-lookup"><span data-stu-id="3c0d8-127">IID</span></span><br/>                      | <span data-ttu-id="3c0d8-128">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="3c0d8-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="3c0d8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c0d8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0d8-130">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="3c0d8-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





