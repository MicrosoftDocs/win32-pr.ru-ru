---
description: Сигнализирует о начале команды DVD Navigator.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0fb723b220bf8aa12baa7133c9985225d6051921
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651648"
---
# <a name="ec_dvd_cmd_start"></a><span data-ttu-id="6e8ec-103">\_Запуск команды DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="6e8ec-103">EC\_DVD\_CMD\_START</span></span>

<span data-ttu-id="6e8ec-104">Сигнализирует о начале команды [DVD Navigator](dvd-navigator-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8ec-104">Signals that a [DVD Navigator](dvd-navigator-filter.md) command has begun.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e8ec-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e8ec-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e8ec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6e8ec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6e8ec-107">Идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="6e8ec-107">Command identifier.</span></span> <span data-ttu-id="6e8ec-108">Передайте этот параметр в метод [**IDvdInfo2:: жеткмдфромевент**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , чтобы получить указатель интерфейса [**идвдкмд**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .</span><span class="sxs-lookup"><span data-stu-id="6e8ec-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="6e8ec-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6e8ec-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6e8ec-110">Значение **HRESULT** , указывающее состояние команды.</span><span class="sxs-lookup"><span data-stu-id="6e8ec-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e8ec-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e8ec-111">Remarks</span></span>

<span data-ttu-id="6e8ec-112">Это событие возникает только в том случае, если приложение устанавливает флаг **\_ \_ \_ SendEvents** для флага DVD cmd в методе [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) , принимающем флаг [**\_ \_ флагов DVD-диска**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .</span><span class="sxs-lookup"><span data-stu-id="6e8ec-112">This event is only fired if your application sets the **DVD\_CMD\_FLAG\_SendEvents** flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="6e8ec-113">Это событие возникает в домене Title.</span><span class="sxs-lookup"><span data-stu-id="6e8ec-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e8ec-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6e8ec-114">Requirements</span></span>



| <span data-ttu-id="6e8ec-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6e8ec-115">Requirement</span></span> | <span data-ttu-id="6e8ec-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6e8ec-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8ec-117">Header</span><span class="sxs-lookup"><span data-stu-id="6e8ec-117">Header</span></span><br/> | <dl> <span data-ttu-id="6e8ec-118"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e8ec-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e8ec-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e8ec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e8ec-120">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="6e8ec-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="6e8ec-121">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="6e8ec-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6e8ec-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="6e8ec-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6e8ec-123">Синхронизация команд DVD</span><span class="sxs-lookup"><span data-stu-id="6e8ec-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




