---
title: Имстскаксевентс Онлеавефуллскринмоде, метод
description: Вызывается, когда клиент выходит из полноэкранного режима. Например, это событие вызывается при нажатии пользователем сочетания клавиш в полноэкранном режиме (CTRL + ALT + BREAK).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онлеавефуллскринмоде
- Службы удаленных рабочих столов метода Онлеавефуллскринмоде, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онлеавефуллскринмоде
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4ee414f2dceba35a17ff86bce03c83d75aab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071767"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a><span data-ttu-id="e6331-107">Метод Имстскаксевентс:: Онлеавефуллскринмоде</span><span class="sxs-lookup"><span data-stu-id="e6331-107">IMsTscAxEvents::OnLeaveFullScreenMode method</span></span>

<span data-ttu-id="e6331-108">Вызывается, когда клиент выходит из полноэкранного режима.</span><span class="sxs-lookup"><span data-stu-id="e6331-108">Called when the client leaves full-screen mode.</span></span> <span data-ttu-id="e6331-109">Например, это событие вызывается при нажатии [пользователем сочетания клавиш](terminal-services-shortcut-keys.md) в полноэкранном режиме (Ctrl + Alt + Break).</span><span class="sxs-lookup"><span data-stu-id="e6331-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6331-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6331-110">Syntax</span></span>


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="e6331-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6331-111">Parameters</span></span>

<span data-ttu-id="e6331-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e6331-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6331-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6331-113">Return value</span></span>

<span data-ttu-id="e6331-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e6331-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6331-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6331-115">Remarks</span></span>

<span data-ttu-id="e6331-116">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e6331-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6331-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e6331-117">Requirements</span></span>



| <span data-ttu-id="e6331-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e6331-118">Requirement</span></span> | <span data-ttu-id="e6331-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e6331-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6331-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6331-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6331-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6331-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e6331-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6331-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6331-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6331-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e6331-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e6331-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6331-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6331-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6331-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e6331-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6331-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6331-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6331-128">IID</span><span class="sxs-lookup"><span data-stu-id="e6331-128">IID</span></span><br/>                      | <span data-ttu-id="e6331-129">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e6331-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e6331-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6331-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6331-131">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="e6331-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





