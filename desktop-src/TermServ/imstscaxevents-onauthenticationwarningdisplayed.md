---
title: Имстскаксевентс Онаусентикатионварнингдисплайед, метод
description: Вызывается перед тем, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "Ошибка сертификата").
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онаусентикатионварнингдисплайед
- Службы удаленных рабочих столов метода Онаусентикатионварнингдисплайед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онаусентикатионварнингдисплайед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135762"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a><span data-ttu-id="eed83-106">Метод Имстскаксевентс:: Онаусентикатионварнингдисплайед</span><span class="sxs-lookup"><span data-stu-id="eed83-106">IMsTscAxEvents::OnAuthenticationWarningDisplayed method</span></span>

<span data-ttu-id="eed83-107">Вызывается перед тем, как элемент управления ActiveX отображает диалоговое окно проверки подлинности (например, диалоговое окно "Ошибка сертификата").</span><span class="sxs-lookup"><span data-stu-id="eed83-107">Called before an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="eed83-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eed83-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a><span data-ttu-id="eed83-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eed83-109">Parameters</span></span>

<span data-ttu-id="eed83-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="eed83-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eed83-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eed83-111">Return value</span></span>

<span data-ttu-id="eed83-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="eed83-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed83-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eed83-113">Remarks</span></span>

<span data-ttu-id="eed83-114">При необходимости можно использовать свойство [**уипарентвиндовхандле**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) интерфейса [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) , чтобы убедиться, что модальное диалоговое окно проверки подлинности будет дочерним по отношению к указанному окну (это может потребоваться, чтобы запретить пользователям использовать другие диалоговые окна во время отображения диалогового окна проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="eed83-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to ensure that the modal authentication dialog to be displayed will be parented by a specified window (this may be necessary to prevent users from using other dialog boxes while the authentication dialog box is displayed).</span></span> <span data-ttu-id="eed83-115">По умолчанию родительским элементом является окно элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="eed83-115">By default, the parent is the ActiveX control window.</span></span>

<span data-ttu-id="eed83-116">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="eed83-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eed83-117">Требования</span><span class="sxs-lookup"><span data-stu-id="eed83-117">Requirements</span></span>



| <span data-ttu-id="eed83-118">Требование</span><span class="sxs-lookup"><span data-stu-id="eed83-118">Requirement</span></span> | <span data-ttu-id="eed83-119">Значение</span><span class="sxs-lookup"><span data-stu-id="eed83-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eed83-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eed83-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eed83-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eed83-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="eed83-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eed83-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eed83-123">Windows Server 2008, Windows Server 2008 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="eed83-123">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="eed83-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eed83-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="eed83-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eed83-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="eed83-126">DLL</span><span class="sxs-lookup"><span data-stu-id="eed83-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eed83-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eed83-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="eed83-128">IID</span><span class="sxs-lookup"><span data-stu-id="eed83-128">IID</span></span><br/>                      | <span data-ttu-id="eed83-129">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="eed83-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="eed83-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eed83-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed83-131">**онаусентикатионварнингдисмиссед**</span><span class="sxs-lookup"><span data-stu-id="eed83-131">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="eed83-132">**уипарентвиндовхандле**</span><span class="sxs-lookup"><span data-stu-id="eed83-132">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="eed83-133">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="eed83-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





