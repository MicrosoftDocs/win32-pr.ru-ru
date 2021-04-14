---
title: Иремотедесктопклиентевентс Онкэйкомбинатионпрессед, метод
description: Вызывается при нажатии специальных сочетаний клавиш в удаленном сеансе.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онкэйкомбинатионпрессед
- Службы удаленных рабочих столов метода Онкэйкомбинатионпрессед, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онкэйкомбинатионпрессед
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415165"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a><span data-ttu-id="28e2a-106">Метод Иремотедесктопклиентевентс:: Онкэйкомбинатионпрессед</span><span class="sxs-lookup"><span data-stu-id="28e2a-106">IRemoteDesktopClientEvents::OnKeyCombinationPressed method</span></span>

<span data-ttu-id="28e2a-107">Вызывается при нажатии специальных сочетаний клавиш в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="28e2a-107">Called when special key combinations are pressed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e2a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28e2a-108">Syntax</span></span>


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a><span data-ttu-id="28e2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28e2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e2a-110">*кэйкомбинатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28e2a-110">*keyCombination* \[in\]</span></span>
<span data-ttu-id="28e2a-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="28e2a-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="28e2a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28e2a-112">Return value</span></span>

<span data-ttu-id="28e2a-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="28e2a-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e2a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="28e2a-114">Requirements</span></span>



| <span data-ttu-id="28e2a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="28e2a-115">Requirement</span></span> | <span data-ttu-id="28e2a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="28e2a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e2a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28e2a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28e2a-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="28e2a-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="28e2a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28e2a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="28e2a-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28e2a-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="28e2a-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="28e2a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="28e2a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28e2a-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="28e2a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="28e2a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28e2a-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28e2a-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="28e2a-125">IID</span><span class="sxs-lookup"><span data-stu-id="28e2a-125">IID</span></span><br/>                      | <span data-ttu-id="28e2a-126">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="28e2a-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28e2a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28e2a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e2a-128">**иремотедесктопклиентевентс**</span><span class="sxs-lookup"><span data-stu-id="28e2a-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





