---
description: Сигнализирует о завершении определенной команды DVD-навигатора.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685163"
---
# <a name="ec_dvd_cmd_end"></a><span data-ttu-id="98682-103">\_Завершение команды DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="98682-103">EC\_DVD\_CMD\_END</span></span>

<span data-ttu-id="98682-104">Сигнализирует о завершении определенной команды [DVD-навигатора](dvd-navigator-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="98682-104">Signals that a particular [DVD Navigator](dvd-navigator-filter.md) command has completed.</span></span>

## <a name="parameters"></a><span data-ttu-id="98682-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="98682-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98682-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="98682-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="98682-107">Идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="98682-107">Command identifier.</span></span> <span data-ttu-id="98682-108">Передайте этот параметр в метод [**IDvdInfo2:: жеткмдфромевент**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , чтобы получить указатель интерфейса [**идвдкмд**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .</span><span class="sxs-lookup"><span data-stu-id="98682-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="98682-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="98682-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="98682-110">Значение **HRESULT** , указывающее состояние команды.</span><span class="sxs-lookup"><span data-stu-id="98682-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98682-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98682-111">Remarks</span></span>

<span data-ttu-id="98682-112">Это событие возникает только в том случае, если приложение устанавливает флаг SendEvents для флага DVD \_ cmd \_ \_ в методе [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) , принимающем флаг [**\_ \_ флагов DVD-диска**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .</span><span class="sxs-lookup"><span data-stu-id="98682-112">This event is only fired if your application sets the DVD\_CMD\_FLAG\_SendEvents flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="98682-113">Это событие возникает в домене Title.</span><span class="sxs-lookup"><span data-stu-id="98682-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="98682-114">Требования</span><span class="sxs-lookup"><span data-stu-id="98682-114">Requirements</span></span>



| <span data-ttu-id="98682-115">Требование</span><span class="sxs-lookup"><span data-stu-id="98682-115">Requirement</span></span> | <span data-ttu-id="98682-116">Значение</span><span class="sxs-lookup"><span data-stu-id="98682-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98682-117">Header</span><span class="sxs-lookup"><span data-stu-id="98682-117">Header</span></span><br/> | <dl> <span data-ttu-id="98682-118"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98682-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98682-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98682-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98682-120">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="98682-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="98682-121">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="98682-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="98682-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="98682-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="98682-123">Синхронизация команд DVD</span><span class="sxs-lookup"><span data-stu-id="98682-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




