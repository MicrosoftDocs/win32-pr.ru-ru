---
title: Имстскаксевентс Онаусентикатионварнингдисмиссед, метод
description: Вызывается после того, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "Ошибка сертификата").
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онаусентикатионварнингдисмиссед
- Службы удаленных рабочих столов метода Онаусентикатионварнингдисмиссед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онаусентикатионварнингдисмиссед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415456"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a><span data-ttu-id="68e57-106">Метод Имстскаксевентс:: Онаусентикатионварнингдисмиссед</span><span class="sxs-lookup"><span data-stu-id="68e57-106">IMsTscAxEvents::OnAuthenticationWarningDismissed method</span></span>

<span data-ttu-id="68e57-107">Вызывается после того, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "Ошибка сертификата").</span><span class="sxs-lookup"><span data-stu-id="68e57-107">Called after an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="68e57-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68e57-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a><span data-ttu-id="68e57-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="68e57-109">Parameters</span></span>

<span data-ttu-id="68e57-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="68e57-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68e57-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68e57-111">Return value</span></span>

<span data-ttu-id="68e57-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="68e57-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68e57-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68e57-113">Remarks</span></span>

<span data-ttu-id="68e57-114">При необходимости можно использовать свойство [**уипарентвиндовхандле**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) интерфейса [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) для возврата всех родительских элементов, которые могли быть выполнены в методе [**онаусентикатионварнингдисплайед**](imstscaxevents-onauthenticationwarningdisplayed.md) .</span><span class="sxs-lookup"><span data-stu-id="68e57-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to revert any parenting that may have been done in the [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) method.</span></span>

<span data-ttu-id="68e57-115">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="68e57-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68e57-116">Требования</span><span class="sxs-lookup"><span data-stu-id="68e57-116">Requirements</span></span>



| <span data-ttu-id="68e57-117">Требование</span><span class="sxs-lookup"><span data-stu-id="68e57-117">Requirement</span></span> | <span data-ttu-id="68e57-118">Значение</span><span class="sxs-lookup"><span data-stu-id="68e57-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68e57-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68e57-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68e57-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68e57-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="68e57-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68e57-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68e57-122">Windows Server 2008, Windows Server 2008 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="68e57-122">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="68e57-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="68e57-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="68e57-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68e57-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68e57-125">DLL</span><span class="sxs-lookup"><span data-stu-id="68e57-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68e57-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68e57-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68e57-127">IID</span><span class="sxs-lookup"><span data-stu-id="68e57-127">IID</span></span><br/>                      | <span data-ttu-id="68e57-128">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="68e57-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="68e57-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68e57-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e57-130">**онаусентикатионварнингдисплайед**</span><span class="sxs-lookup"><span data-stu-id="68e57-130">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="68e57-131">**уипарентвиндовхандле**</span><span class="sxs-lookup"><span data-stu-id="68e57-131">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="68e57-132">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="68e57-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





