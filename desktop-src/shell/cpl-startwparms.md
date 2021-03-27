---
description: Отправляется уведомление Кплапплет о том, что пользователь выбрал значок, связанный с заданным диалоговым окном. Кплапплет должен отобразить соответствующее диалоговое окно и выполнить все определяемые пользователем задачи.
title: Сообщение CPL_STARTWPARMS (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990958"
---
# <a name="cpl_startwparms-message"></a><span data-ttu-id="6b2e7-104">\_Сообщение CPL стартвпармс</span><span class="sxs-lookup"><span data-stu-id="6b2e7-104">CPL\_STARTWPARMS message</span></span>

<span data-ttu-id="6b2e7-105">Отправляется уведомление [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) о том, что пользователь выбрал значок, связанный с заданным диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="6b2e7-105">Sent to notify [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) that the user has chosen the icon associated with a given dialog box.</span></span> <span data-ttu-id="6b2e7-106">**Кплапплет** должен отобразить соответствующее диалоговое окно и выполнить все определяемые пользователем задачи.</span><span class="sxs-lookup"><span data-stu-id="6b2e7-106">**CPlApplet** should display the corresponding dialog box and carry out any user-specified tasks.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b2e7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b2e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b2e7-108">*уаппнум*</span><span class="sxs-lookup"><span data-stu-id="6b2e7-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="6b2e7-109">Число в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6b2e7-109">The dialog box number.</span></span> <span data-ttu-id="6b2e7-110">Это число должно находиться в диапазоне от нуля до значения, возвращенного в ответ на сообщение [**CPL \_ NOCOUNT**](cpl-getcount.md) (CPL \_ -count – 1).</span><span class="sxs-lookup"><span data-stu-id="6b2e7-110">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="6b2e7-111">*лпсзекстра*</span><span class="sxs-lookup"><span data-stu-id="6b2e7-111">*lpszExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="6b2e7-112">Строка с дополнительными указаниями для выполнения.</span><span class="sxs-lookup"><span data-stu-id="6b2e7-112">A string with additional directions for execution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b2e7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b2e7-113">Return value</span></span>

<span data-ttu-id="6b2e7-114">Возвращает **значение true** , если сообщение было обработано, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6b2e7-114">Returns **TRUE** if the message was handled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b2e7-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b2e7-115">Remarks</span></span>

<span data-ttu-id="6b2e7-116">**CPL \_ СТАРТВПАРМС** похож на [**CPL \_ дблклк**](cpl-dblclk.md) , но позволяет передавать строку [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) вместо **int**. Эту строку можно использовать в качестве гибкого способа предоставления подробных инструкций по выполнению.</span><span class="sxs-lookup"><span data-stu-id="6b2e7-116">**CPL\_STARTWPARMS** is similar to [**CPL\_DBLCLK**](cpl-dblclk.md) but allows you to pass a string to [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) instead of an **int**. You can use this string as a flexible way to provide detailed directions for execution.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b2e7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6b2e7-117">Requirements</span></span>



| <span data-ttu-id="6b2e7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6b2e7-118">Requirement</span></span> | <span data-ttu-id="6b2e7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6b2e7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b2e7-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b2e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2e7-121">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b2e7-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="6b2e7-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b2e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2e7-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b2e7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b2e7-124">Header</span><span class="sxs-lookup"><span data-stu-id="6b2e7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b2e7-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b2e7-125"><dt>Cpl.h</dt></span></span> </dl> |



 

 
