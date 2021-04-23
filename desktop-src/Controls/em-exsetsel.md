---
title: Сообщение EM_EXSETSEL (RichEdit. h)
description: Выбирает диапазон символов или объектов модели COM в элементе управления Microsoft Rich Edit.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- Элементы управления Windows для EM_EXSETSEL сообщений
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892173"
---
# <a name="em_exsetsel-message"></a><span data-ttu-id="3f59e-104">\_Сообщение ЕКССЕТСЕЛ EM</span><span class="sxs-lookup"><span data-stu-id="3f59e-104">EM\_EXSETSEL message</span></span>

<span data-ttu-id="3f59e-105">Выбирает диапазон символов или объектов модели COM в элементе управления Microsoft Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3f59e-105">Selects a range of characters or Component Object Model (COM) objects in a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f59e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f59e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f59e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f59e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f59e-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3f59e-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3f59e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f59e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f59e-110">Структура [**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange) , указывающая диапазон выбора.</span><span class="sxs-lookup"><span data-stu-id="3f59e-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that specifies the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f59e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f59e-111">Return value</span></span>

<span data-ttu-id="3f59e-112">Возвращаемое значение является фактически установленным выделением.</span><span class="sxs-lookup"><span data-stu-id="3f59e-112">The return value is the selection that is actually set.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f59e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3f59e-113">Requirements</span></span>



| <span data-ttu-id="3f59e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3f59e-114">Requirement</span></span> | <span data-ttu-id="3f59e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3f59e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f59e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f59e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3f59e-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f59e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f59e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f59e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3f59e-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3f59e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f59e-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f59e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f59e-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f59e-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





