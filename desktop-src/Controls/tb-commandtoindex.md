---
title: Сообщение TB_COMMANDTOINDEX (Коммктрл. h)
description: Возвращает отсчитываемый от нуля индекс для кнопки, связанной с указанным идентификатором команды.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- Элементы управления Windows для TB_COMMANDTOINDEX сообщений
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137850"
---
# <a name="tb_commandtoindex-message"></a><span data-ttu-id="52e27-104">\_Сообщение КОММАНДТОИНДЕКС ТБ</span><span class="sxs-lookup"><span data-stu-id="52e27-104">TB\_COMMANDTOINDEX message</span></span>

<span data-ttu-id="52e27-105">Возвращает отсчитываемый от нуля индекс для кнопки, связанной с указанным идентификатором команды.</span><span class="sxs-lookup"><span data-stu-id="52e27-105">Retrieves the zero-based index for the button associated with the specified command identifier.</span></span>

## <a name="parameters"></a><span data-ttu-id="52e27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="52e27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52e27-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52e27-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52e27-108">Идентификатор команды, связанный с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="52e27-108">Command identifier associated with the button.</span></span>

</dd> <dt>

<span data-ttu-id="52e27-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52e27-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="52e27-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="52e27-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52e27-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52e27-111">Return value</span></span>

<span data-ttu-id="52e27-112">Возвращает отсчитываемый от нуля индекс для кнопки или-1, если указанный идентификатор команды является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="52e27-112">Returns the zero-based index for the button or -1 if the specified command identifier is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="52e27-113">Требования</span><span class="sxs-lookup"><span data-stu-id="52e27-113">Requirements</span></span>



| <span data-ttu-id="52e27-114">Требование</span><span class="sxs-lookup"><span data-stu-id="52e27-114">Requirement</span></span> | <span data-ttu-id="52e27-115">Значение</span><span class="sxs-lookup"><span data-stu-id="52e27-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52e27-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52e27-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52e27-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52e27-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52e27-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52e27-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52e27-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52e27-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52e27-120">Header</span><span class="sxs-lookup"><span data-stu-id="52e27-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52e27-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="52e27-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





