---
title: Сообщение MCM_GETCALENDARGRIDINFO (Коммктрл. h)
description: Возвращает сведения о сетке календаря.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- Элементы управления Windows для MCM_GETCALENDARGRIDINFO сообщений
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804145"
---
# <a name="mcm_getcalendargridinfo-message"></a><span data-ttu-id="57e34-104">\_Сообщение MCM жеткалендаргридинфо</span><span class="sxs-lookup"><span data-stu-id="57e34-104">MCM\_GETCALENDARGRIDINFO message</span></span>

<span data-ttu-id="57e34-105">Возвращает сведения о сетке календаря.</span><span class="sxs-lookup"><span data-stu-id="57e34-105">Gets information about a calendar grid.</span></span>

## <a name="parameters"></a><span data-ttu-id="57e34-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57e34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57e34-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57e34-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57e34-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="57e34-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="57e34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57e34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57e34-110">Указатель на структуру [**мкгридинфо**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) , содержащую сведения о сетке календаря.</span><span class="sxs-lookup"><span data-stu-id="57e34-110">Pointer to an [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) structure that contains information about the calendar grid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57e34-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57e34-111">Return value</span></span>

<span data-ttu-id="57e34-112">**Значение true** , если выполнено успешно; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="57e34-112">**TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="57e34-113">Требования</span><span class="sxs-lookup"><span data-stu-id="57e34-113">Requirements</span></span>



| <span data-ttu-id="57e34-114">Требование</span><span class="sxs-lookup"><span data-stu-id="57e34-114">Requirement</span></span> | <span data-ttu-id="57e34-115">Значение</span><span class="sxs-lookup"><span data-stu-id="57e34-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57e34-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57e34-116">Minimum supported client</span></span><br/> | <span data-ttu-id="57e34-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57e34-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57e34-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57e34-118">Minimum supported server</span></span><br/> | <span data-ttu-id="57e34-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="57e34-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57e34-120">Header</span><span class="sxs-lookup"><span data-stu-id="57e34-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="57e34-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="57e34-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





