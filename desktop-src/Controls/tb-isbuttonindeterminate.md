---
title: Сообщение TB_ISBUTTONINDETERMINATE (Коммктрл. h)
description: Определяет, является ли указанная кнопка на панели инструментов неопределенной.
ms.assetid: b4d759b3-cdbc-417b-9da4-4ed9edc38c0e
keywords:
- Элементы управления Windows для TB_ISBUTTONINDETERMINATE сообщений
topic_type:
- apiref
api_name:
- TB_ISBUTTONINDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc024efcad9f0f48ae4882b019269903c249bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071379"
---
# <a name="tb_isbuttonindeterminate-message"></a><span data-ttu-id="681ec-104">\_Сообщение ИСБУТТОНИНДЕТЕРМИНАТЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="681ec-104">TB\_ISBUTTONINDETERMINATE message</span></span>

<span data-ttu-id="681ec-105">Определяет, является ли указанная кнопка на панели инструментов неопределенной.</span><span class="sxs-lookup"><span data-stu-id="681ec-105">Determines whether the specified button in a toolbar is indeterminate.</span></span>

## <a name="parameters"></a><span data-ttu-id="681ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="681ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="681ec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="681ec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="681ec-108">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="681ec-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="681ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="681ec-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="681ec-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="681ec-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="681ec-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="681ec-111">Return value</span></span>

<span data-ttu-id="681ec-112">Возвращает ненулевое значение, если кнопка является неопределенной, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="681ec-112">Returns nonzero if the button is indeterminate, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="681ec-113">Требования</span><span class="sxs-lookup"><span data-stu-id="681ec-113">Requirements</span></span>



| <span data-ttu-id="681ec-114">Требование</span><span class="sxs-lookup"><span data-stu-id="681ec-114">Requirement</span></span> | <span data-ttu-id="681ec-115">Значение</span><span class="sxs-lookup"><span data-stu-id="681ec-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="681ec-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="681ec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="681ec-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="681ec-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="681ec-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="681ec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="681ec-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="681ec-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="681ec-120">Header</span><span class="sxs-lookup"><span data-stu-id="681ec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="681ec-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="681ec-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





