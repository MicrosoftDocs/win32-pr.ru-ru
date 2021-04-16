---
title: Иремотедесктопклиентевентс Онтаучпоинтеркурсормовед, метод
description: Вызывается, когда курсор сенсорного указателя переместился и свойство Евентсенаблед имеет значение true.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онтаучпоинтеркурсормовед
- Службы удаленных рабочих столов метода Онтаучпоинтеркурсормовед, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онтаучпоинтеркурсормовед
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672663"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a><span data-ttu-id="def23-106">Метод Иремотедесктопклиентевентс:: Онтаучпоинтеркурсормовед</span><span class="sxs-lookup"><span data-stu-id="def23-106">IRemoteDesktopClientEvents::OnTouchPointerCursorMoved method</span></span>

<span data-ttu-id="def23-107">Вызывается, когда курсор сенсорного указателя переместился и свойство [**евентсенаблед**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="def23-107">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

## <a name="syntax"></a><span data-ttu-id="def23-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="def23-108">Syntax</span></span>


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a><span data-ttu-id="def23-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="def23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def23-110">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="def23-110">*x* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="def23-111">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="def23-111">*y* \[in\]</span></span>
<span data-ttu-id="def23-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="def23-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="def23-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="def23-113">Return value</span></span>

<span data-ttu-id="def23-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="def23-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="def23-115">Требования</span><span class="sxs-lookup"><span data-stu-id="def23-115">Requirements</span></span>



| <span data-ttu-id="def23-116">Требование</span><span class="sxs-lookup"><span data-stu-id="def23-116">Requirement</span></span> | <span data-ttu-id="def23-117">Значение</span><span class="sxs-lookup"><span data-stu-id="def23-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def23-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="def23-118">Minimum supported client</span></span><br/> | <span data-ttu-id="def23-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="def23-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="def23-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="def23-120">Minimum supported server</span></span><br/> | <span data-ttu-id="def23-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="def23-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="def23-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="def23-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="def23-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="def23-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="def23-124">DLL</span><span class="sxs-lookup"><span data-stu-id="def23-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def23-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="def23-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="def23-126">IID</span><span class="sxs-lookup"><span data-stu-id="def23-126">IID</span></span><br/>                      | <span data-ttu-id="def23-127">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="def23-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="def23-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="def23-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def23-129">**иремотедесктопклиентевентс**</span><span class="sxs-lookup"><span data-stu-id="def23-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

