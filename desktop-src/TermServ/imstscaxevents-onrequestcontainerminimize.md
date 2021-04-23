---
title: Имстскаксевентс Онрекуестконтаинерминимизе, метод
description: Вызывается, когда пользователь нажимает кнопку сворачивания на панели подключения в полноэкранном режиме. Срабатывание этого события является запрос, в котором приложение контейнера свернется само по себе.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онрекуестконтаинерминимизе
- Службы удаленных рабочих столов метода Онрекуестконтаинерминимизе, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онрекуестконтаинерминимизе
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415753"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a><span data-ttu-id="8b2e9-107">Метод Имстскаксевентс:: Онрекуестконтаинерминимизе</span><span class="sxs-lookup"><span data-stu-id="8b2e9-107">IMsTscAxEvents::OnRequestContainerMinimize method</span></span>

<span data-ttu-id="8b2e9-108">Вызывается, когда пользователь нажимает кнопку **сворачивания** на панели подключения в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="8b2e9-108">Called when the user presses the **Minimize** button on the connection bar in full-screen mode.</span></span> <span data-ttu-id="8b2e9-109">Срабатывание этого события является запрос, в котором приложение контейнера свернется само по себе.</span><span class="sxs-lookup"><span data-stu-id="8b2e9-109">The firing of this event is a request that the container application minimize itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b2e9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b2e9-110">Syntax</span></span>


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a><span data-ttu-id="8b2e9-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b2e9-111">Parameters</span></span>

<span data-ttu-id="8b2e9-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8b2e9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b2e9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b2e9-113">Return value</span></span>

<span data-ttu-id="8b2e9-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8b2e9-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b2e9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b2e9-115">Remarks</span></span>

<span data-ttu-id="8b2e9-116">Этот метод будет вызываться только при включенном полноэкранном режиме, поддерживающем контейнер. Дополнительные сведения см. в разделе [**имстскадванцедсеттингс::p UT \_ контаинерхандледфуллскрин**](imstscadvancedsettings-containerhandledfullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="8b2e9-116">This method will only be called if the container-handled full-screen mode is enabled - see [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b2e9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8b2e9-117">Requirements</span></span>



| <span data-ttu-id="8b2e9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8b2e9-118">Requirement</span></span> | <span data-ttu-id="8b2e9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8b2e9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2e9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b2e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8b2e9-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b2e9-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8b2e9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b2e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8b2e9-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b2e9-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8b2e9-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8b2e9-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b2e9-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b2e9-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b2e9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8b2e9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b2e9-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b2e9-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b2e9-128">IID</span><span class="sxs-lookup"><span data-stu-id="8b2e9-128">IID</span></span><br/>                      | <span data-ttu-id="8b2e9-129">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="8b2e9-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8b2e9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b2e9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b2e9-131">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="8b2e9-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





