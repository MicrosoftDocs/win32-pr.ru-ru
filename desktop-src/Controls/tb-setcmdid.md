---
title: Сообщение TB_SETCMDID (Коммктрл. h)
description: Задает идентификатор команды для кнопки панели инструментов.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- Элементы управления Windows для TB_SETCMDID сообщений
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654517"
---
# <a name="tb_setcmdid-message"></a><span data-ttu-id="c9781-104">\_Сообщение СЕТКМДИД ТБ</span><span class="sxs-lookup"><span data-stu-id="c9781-104">TB\_SETCMDID message</span></span>

<span data-ttu-id="c9781-105">Задает идентификатор команды для кнопки панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="c9781-105">Sets the command identifier of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9781-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9781-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9781-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9781-108">Отсчитываемый от нуля индекс кнопки, идентификатор команды которого необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="c9781-108">Zero-based index of the button whose command identifier is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="c9781-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9781-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9781-110">Идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="c9781-110">Command identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9781-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9781-111">Return value</span></span>

<span data-ttu-id="c9781-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c9781-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9781-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c9781-113">Requirements</span></span>



| <span data-ttu-id="c9781-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c9781-114">Requirement</span></span> | <span data-ttu-id="c9781-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c9781-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9781-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9781-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c9781-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9781-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9781-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9781-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c9781-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9781-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9781-120">Header</span><span class="sxs-lookup"><span data-stu-id="c9781-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9781-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9781-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





