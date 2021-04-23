---
title: Иакцессибилитидоккингсервице Жетаваилаблесизе, метод
description: Возвращает размеры, доступные для закрепления окна специальных возможностей на мониторе.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- COM-метод Жетаваилаблесизе
- Метод Жетаваилаблесизе COM, интерфейс Иакцессибилитидоккингсервице
- Интерфейс Иакцессибилитидоккингсервице COM, метод Жетаваилаблесизе
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068942"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a><span data-ttu-id="fc39d-106">Метод Иакцессибилитидоккингсервице:: Жетаваилаблесизе</span><span class="sxs-lookup"><span data-stu-id="fc39d-106">IAccessibilityDockingService::GetAvailableSize method</span></span>

<span data-ttu-id="fc39d-107">Возвращает размеры, доступные для закрепления окна специальных возможностей на мониторе.</span><span class="sxs-lookup"><span data-stu-id="fc39d-107">Gets the dimensions available for docking an accessibility window on a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc39d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc39d-108">Syntax</span></span>


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a><span data-ttu-id="fc39d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc39d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc39d-110">*хмонитор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc39d-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc39d-111">Указывает монитор, для которого будет получен доступный размер закрепления.</span><span class="sxs-lookup"><span data-stu-id="fc39d-111">Specifies the monitor for which the available docking size will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="fc39d-112">*пумаксхеигхт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc39d-112">*puMaxHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc39d-113">При успешном выполнении задайте максимальную высоту, доступную для закрепления на заданном *хмонитор*, в пикселях.</span><span class="sxs-lookup"><span data-stu-id="fc39d-113">On success, set to the maximum height available for docking on the specified *hMonitor*, in pixels.</span></span>

<span data-ttu-id="fc39d-114">В случае сбоя установите нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="fc39d-114">On failure, set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fc39d-115">*пуфикседвидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc39d-115">*puFixedWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc39d-116">При успешном выполнении задайте фиксированную ширину, доступную для закрепления в заданном *хмонитор*, в пикселях.</span><span class="sxs-lookup"><span data-stu-id="fc39d-116">On success, set to the fixed width available for docking on the specified *hMonitor*, in pixels.</span></span> <span data-ttu-id="fc39d-117">Любое окно, прикрепленное к этому *хмонитор* , будет иметь ширину.</span><span class="sxs-lookup"><span data-stu-id="fc39d-117">Any window docked to this *hMonitor* will be sized to this width.</span></span>

<span data-ttu-id="fc39d-118">В случае сбоя установите нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="fc39d-118">On failure, set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc39d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc39d-119">Return value</span></span>



| <span data-ttu-id="fc39d-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fc39d-120">Return code</span></span>                                                                                                                          | <span data-ttu-id="fc39d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="fc39d-121">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc39d-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fc39d-122"><dt>**S\_OK**</dt></span></span> </dl>                                                 | <span data-ttu-id="fc39d-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fc39d-123">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="fc39d-124"><dt>**HRESULT \_ из \_ Win32 (ошибка: \_ Недопустимый \_ \_ маркер монитора)**</dt></span><span class="sxs-lookup"><span data-stu-id="fc39d-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_MONITOR\_HANDLE)**</dt></span></span> </dl> | <span data-ttu-id="fc39d-125">Монитор, указанный в обработчике монитора, не поддерживает прикрепление.</span><span class="sxs-lookup"><span data-stu-id="fc39d-125">The monitor specified by the monitor handle does not support docking.</span></span><br/> |



 

<span data-ttu-id="fc39d-126">Если либо *пумаксхеигхт* , либо *пуфикседвидс* имеют значение null, произойдет нарушение прав доступа.</span><span class="sxs-lookup"><span data-stu-id="fc39d-126">If either *puMaxHeight* or *puFixedWidth* are null, an access violation will occur.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc39d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc39d-127">Remarks</span></span>

<span data-ttu-id="fc39d-128">Окна специальных возможностей могут быть прикреплены только к монитору, который содержит не менее 768 вертикальных пикселей на экране.</span><span class="sxs-lookup"><span data-stu-id="fc39d-128">Accessibility windows can only be docked to a monitor that has at least 768 vertical screen pixels.</span></span> <span data-ttu-id="fc39d-129">Этот API не позволяет закреплять такие окна с высотой, что приведет к тому, что приложения Магазина Windows будут иметь менее 768 вертикальных пикселей на экране.</span><span class="sxs-lookup"><span data-stu-id="fc39d-129">This API will not allow such windows to be docked with a height that would cause Windows Store apps to have less than 768 vertical screen pixels.</span></span>

## <a name="examples"></a><span data-ttu-id="fc39d-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="fc39d-130">Examples</span></span>


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a><span data-ttu-id="fc39d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc39d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc39d-132">**иакцессибилитидоккингсервице**</span><span class="sxs-lookup"><span data-stu-id="fc39d-132">**IAccessibilityDockingService**</span></span>](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





