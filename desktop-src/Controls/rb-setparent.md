---
title: Сообщение RB_SETPARENT (Коммктрл. h)
description: Задает родительское окно элемента управления главной панели.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- Элементы управления Windows для RB_SETPARENT сообщений
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892270"
---
# <a name="rb_setparent-message"></a><span data-ttu-id="08097-104">\_Сообщение СЕТПАРЕНТ RB</span><span class="sxs-lookup"><span data-stu-id="08097-104">RB\_SETPARENT message</span></span>

<span data-ttu-id="08097-105">Задает родительское окно элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="08097-105">Sets a rebar control's parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="08097-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08097-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08097-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08097-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08097-108">Обрабатываемое родительское окно.</span><span class="sxs-lookup"><span data-stu-id="08097-108">Handle to the parent window to be set.</span></span>

</dd> <dt>

<span data-ttu-id="08097-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08097-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="08097-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="08097-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08097-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08097-111">Return value</span></span>

<span data-ttu-id="08097-112">Возвращает маркер предыдущего родительского окна или **значение NULL** , если предыдущий родительский элемент отсутствует.</span><span class="sxs-lookup"><span data-stu-id="08097-112">Returns the handle to the previous parent window, or **NULL** if there is no previous parent.</span></span>

## <a name="remarks"></a><span data-ttu-id="08097-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08097-113">Remarks</span></span>

<span data-ttu-id="08097-114">Элемент управления "Главная панель" отправляет сообщения уведомления в окно, указанное этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="08097-114">The rebar control sends notification messages to the window you specify with this message.</span></span> <span data-ttu-id="08097-115">Это сообщение фактически не изменяет родительский элемент управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="08097-115">This message does not actually change the parent of the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="08097-116">Требования</span><span class="sxs-lookup"><span data-stu-id="08097-116">Requirements</span></span>



| <span data-ttu-id="08097-117">Требование</span><span class="sxs-lookup"><span data-stu-id="08097-117">Requirement</span></span> | <span data-ttu-id="08097-118">Значение</span><span class="sxs-lookup"><span data-stu-id="08097-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08097-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08097-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08097-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08097-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08097-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08097-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08097-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08097-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08097-123">Header</span><span class="sxs-lookup"><span data-stu-id="08097-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08097-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="08097-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





