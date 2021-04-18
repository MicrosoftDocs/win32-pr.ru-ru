---
title: Иремотедесктопклиентевентс Онадминмессажерецеивед, метод
description: Вызывается, когда клиентский элемент управления получает административное сообщение.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онадминмессажерецеивед
- Службы удаленных рабочих столов метода Онадминмессажерецеивед, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онадминмессажерецеивед
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415852"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a><span data-ttu-id="d0227-106">Метод Иремотедесктопклиентевентс:: Онадминмессажерецеивед</span><span class="sxs-lookup"><span data-stu-id="d0227-106">IRemoteDesktopClientEvents::OnAdminMessageReceived method</span></span>

<span data-ttu-id="d0227-107">Вызывается, когда клиентский элемент управления получает административное сообщение.</span><span class="sxs-lookup"><span data-stu-id="d0227-107">Called when the client control receives an administrative message.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0227-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0227-108">Syntax</span></span>


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a><span data-ttu-id="d0227-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0227-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0227-110">*админмессаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0227-110">*adminMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0227-111">Сообщение.</span><span class="sxs-lookup"><span data-stu-id="d0227-111">The message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0227-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0227-112">Return value</span></span>

<span data-ttu-id="d0227-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d0227-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0227-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d0227-114">Requirements</span></span>



| <span data-ttu-id="d0227-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d0227-115">Requirement</span></span> | <span data-ttu-id="d0227-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d0227-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0227-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0227-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d0227-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d0227-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="d0227-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0227-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d0227-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0227-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="d0227-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d0227-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0227-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0227-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="d0227-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d0227-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0227-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0227-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="d0227-125">IID</span><span class="sxs-lookup"><span data-stu-id="d0227-125">IID</span></span><br/>                      | <span data-ttu-id="d0227-126">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="d0227-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0227-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0227-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0227-128">**иремотедесктопклиентевентс**</span><span class="sxs-lookup"><span data-stu-id="d0227-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





