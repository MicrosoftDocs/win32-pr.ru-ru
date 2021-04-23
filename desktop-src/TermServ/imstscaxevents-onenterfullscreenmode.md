---
title: Имстскаксевентс Онентерфуллскринмоде, метод
description: Вызывается, когда клиент переходит в полноэкранный режим. Например, это событие вызывается при нажатии пользователем сочетания клавиш в полноэкранном режиме (CTRL + ALT + BREAK).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онентерфуллскринмоде
- Службы удаленных рабочих столов метода Онентерфуллскринмоде, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онентерфуллскринмоде
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226054fc7b1371bb088deb70ec9e87ea5a340b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988855"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a><span data-ttu-id="913ab-107">Метод Имстскаксевентс:: Онентерфуллскринмоде</span><span class="sxs-lookup"><span data-stu-id="913ab-107">IMsTscAxEvents::OnEnterFullScreenMode method</span></span>

<span data-ttu-id="913ab-108">Вызывается, когда клиент переходит в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="913ab-108">Called when the client enters full-screen mode.</span></span> <span data-ttu-id="913ab-109">Например, это событие вызывается при нажатии [пользователем сочетания клавиш](terminal-services-shortcut-keys.md) в полноэкранном режиме (Ctrl + Alt + Break).</span><span class="sxs-lookup"><span data-stu-id="913ab-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="913ab-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="913ab-110">Syntax</span></span>


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="913ab-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="913ab-111">Parameters</span></span>

<span data-ttu-id="913ab-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="913ab-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="913ab-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="913ab-113">Return value</span></span>

<span data-ttu-id="913ab-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="913ab-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="913ab-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="913ab-115">Remarks</span></span>

<span data-ttu-id="913ab-116">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="913ab-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="913ab-117">Требования</span><span class="sxs-lookup"><span data-stu-id="913ab-117">Requirements</span></span>



| <span data-ttu-id="913ab-118">Требование</span><span class="sxs-lookup"><span data-stu-id="913ab-118">Requirement</span></span> | <span data-ttu-id="913ab-119">Значение</span><span class="sxs-lookup"><span data-stu-id="913ab-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="913ab-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="913ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="913ab-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="913ab-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="913ab-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="913ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="913ab-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="913ab-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="913ab-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="913ab-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="913ab-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="913ab-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="913ab-126">DLL</span><span class="sxs-lookup"><span data-stu-id="913ab-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="913ab-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="913ab-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="913ab-128">IID</span><span class="sxs-lookup"><span data-stu-id="913ab-128">IID</span></span><br/>                      | <span data-ttu-id="913ab-129">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="913ab-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="913ab-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="913ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913ab-131">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="913ab-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





