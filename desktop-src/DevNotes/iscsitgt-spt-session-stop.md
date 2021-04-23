---
description: Используется с \_ \_ управляющим кодом ioctl SCSI минипорта IOCTL и ктлкоде \_ искситгт \_ СПТ \_ Session \_ End (0x101) для завершения сеанса.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Структура ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "103914291"
---
# <a name="iscsitgt_spt_session_stop-structure"></a><span data-ttu-id="8254f-103">\_Структура искситгт СПТ \_ сеанса \_</span><span class="sxs-lookup"><span data-stu-id="8254f-103">ISCSITGT\_SPT\_SESSION\_STOP structure</span></span>

<span data-ttu-id="8254f-104">\[Следующая структура доступна для использования в Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="8254f-104">\[The following structure is available for use in Windows Server 2012 R2.</span></span> <span data-ttu-id="8254f-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="8254f-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="8254f-106">Используется с управляющим кодом ioctl [**\_ SCSI \_ МИНИПОРТА**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL и ктлкоде \_ искситгт \_ СПТ \_ Session \_ End (0x101) для завершения сеанса.</span><span class="sxs-lookup"><span data-stu-id="8254f-106">Used with the [**IOCTL\_SCSI\_MINIPORT**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL and the CTLCODE\_ISCSITGT\_SPT\_SESSION\_END (0x101) control code to stop a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="8254f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8254f-107">Syntax</span></span>


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a><span data-ttu-id="8254f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8254f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8254f-109">**Header**</span><span class="sxs-lookup"><span data-stu-id="8254f-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="8254f-110">Обязательный заголовок.</span><span class="sxs-lookup"><span data-stu-id="8254f-110">Mandatory header.</span></span>

</dd> <dt>

<span data-ttu-id="8254f-111">**итнексушандле**</span><span class="sxs-lookup"><span data-stu-id="8254f-111">**ITNexusHandle**</span></span>
</dt> <dd>

<span data-ttu-id="8254f-112">Непрозрачный маркер, представляющий сеанс.</span><span class="sxs-lookup"><span data-stu-id="8254f-112">An opaque handle representing a session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8254f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8254f-113">Requirements</span></span>



| <span data-ttu-id="8254f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8254f-114">Requirement</span></span> | <span data-ttu-id="8254f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8254f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8254f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8254f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8254f-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8254f-117">None supported</span></span><br/>                               |
| <span data-ttu-id="8254f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8254f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8254f-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8254f-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8254f-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8254f-120">End of client support</span></span><br/>    | <span data-ttu-id="8254f-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8254f-121">None supported</span></span><br/>                               |
| <span data-ttu-id="8254f-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8254f-122">End of server support</span></span><br/>    | <span data-ttu-id="8254f-123">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8254f-123">Windows Server 2012 R2</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8254f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8254f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8254f-125">Передача цели iSCSI</span><span class="sxs-lookup"><span data-stu-id="8254f-125">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="8254f-126">**\_элемент управления вводом-выводом СРБ \_**</span><span class="sxs-lookup"><span data-stu-id="8254f-126">**SRB\_IO\_CONTROL**</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
