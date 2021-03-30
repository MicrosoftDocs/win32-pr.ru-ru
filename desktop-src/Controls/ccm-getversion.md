---
title: Сообщение CCM_GETVERSION (Коммктрл. h)
description: Возвращает номер версии элемента управления, заданного последним \_ сообщением CCM сетверсион.
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- Элементы управления Windows для CCM_GETVERSION сообщений
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136454"
---
# <a name="ccm_getversion-message"></a><span data-ttu-id="b59b9-104">Сообщение CCM для \_ версии</span><span class="sxs-lookup"><span data-stu-id="b59b9-104">CCM\_GETVERSION message</span></span>

<span data-ttu-id="b59b9-105">Возвращает номер версии элемента управления, заданного последним сообщением [**CCM \_ сетверсион**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b59b9-105">Gets the version number for a control set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="b59b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b59b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b59b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b59b9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b59b9-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b59b9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b59b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b59b9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b59b9-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b59b9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b59b9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b59b9-111">Return value</span></span>

<span data-ttu-id="b59b9-112">Возвращает номер версии, заданный последним сообщением [**CCM \_ сетверсион**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b59b9-112">Returns the version number set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="b59b9-113">Если такое сообщение не было отправлено, оно возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b59b9-113">If no such message has been sent, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b59b9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b59b9-114">Remarks</span></span>

<span data-ttu-id="b59b9-115">Это сообщение не возвращает версию библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="b59b9-115">This message does not return the DLL version.</span></span> <span data-ttu-id="b59b9-116">Сведения об использовании [**дллжетверсион**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) для получения текущей версии DLL см. в статье [версии оболочки](common-control-versions.md) .</span><span class="sxs-lookup"><span data-stu-id="b59b9-116">See [Shell Versions](common-control-versions.md) for a discussion of how to use [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) to retrieve the current DLL version.</span></span>

> [!Note]  
> <span data-ttu-id="b59b9-117">Номер версии задается для каждого элемента управления и может отличаться для всех элементов управления.</span><span class="sxs-lookup"><span data-stu-id="b59b9-117">The version number is set on a control by control basis, and may not be the same for all controls.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b59b9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b59b9-118">Requirements</span></span>



| <span data-ttu-id="b59b9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b59b9-119">Requirement</span></span> | <span data-ttu-id="b59b9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b59b9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b59b9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b59b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b59b9-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b59b9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b59b9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b59b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b59b9-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b59b9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b59b9-125">Header</span><span class="sxs-lookup"><span data-stu-id="b59b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b59b9-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b59b9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

