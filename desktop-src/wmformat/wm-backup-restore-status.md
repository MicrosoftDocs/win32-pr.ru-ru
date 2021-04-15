---
title: Структура WM_BACKUP_RESTORE_STATUS (Вмдрмсдк. h)
description: '\_Структура состояния восстановления резервной копии WM \_ \_ содержит сведения об ожидающей операции резервного копирования или восстановления лицензий.'
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- Формат WM_BACKUP_RESTORE_STATUS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708426"
---
# <a name="wm_backup_restore_status-structure"></a><span data-ttu-id="876d8-105">\_ \_ Структура состояния восстановления резервной копии WM \_</span><span class="sxs-lookup"><span data-stu-id="876d8-105">WM\_BACKUP\_RESTORE\_STATUS structure</span></span>

<span data-ttu-id="876d8-106">Структура **\_ \_ \_ состояния восстановления резервной копии WM** содержит сведения об ожидающей операции резервного копирования или восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="876d8-106">The **WM\_BACKUP\_RESTORE\_STATUS** structure holds information about a pending license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="876d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="876d8-107">Syntax</span></span>


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a><span data-ttu-id="876d8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="876d8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="876d8-109">**естатус**</span><span class="sxs-lookup"><span data-stu-id="876d8-109">**eStatus**</span></span>
</dt> <dd>

<span data-ttu-id="876d8-110">Член перечисления [**\_ состояния Msdrm**](msdrm-status.md) , указывающий состояние.</span><span class="sxs-lookup"><span data-stu-id="876d8-110">Member of the [**MSDRM\_STATUS**](msdrm-status.md) enumeration specifying the status.</span></span>

</dd> <dt>

<span data-ttu-id="876d8-111">**бстреррор**</span><span class="sxs-lookup"><span data-stu-id="876d8-111">**bstrError**</span></span>
</dt> <dd>

<span data-ttu-id="876d8-112">Строка, содержащая ошибку.</span><span class="sxs-lookup"><span data-stu-id="876d8-112">String containing the error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="876d8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="876d8-113">Remarks</span></span>

<span data-ttu-id="876d8-114">Эта структура получается при вызове метода [**ивмдрмлиценсебаккупресторестатус::-Status**](iwmdrmlicensebackuprestorestatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="876d8-114">This structure is received when you call the [**IWMDRMLicenseBackupRestoreStatus::GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) method.</span></span> <span data-ttu-id="876d8-115">Он содержит состояние ожидающей операции резервного копирования или восстановления во время вызова.</span><span class="sxs-lookup"><span data-stu-id="876d8-115">It contains the status of the pending backup or restore operation at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="876d8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="876d8-116">Requirements</span></span>



| <span data-ttu-id="876d8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="876d8-117">Requirement</span></span> | <span data-ttu-id="876d8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="876d8-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="876d8-119">Header</span><span class="sxs-lookup"><span data-stu-id="876d8-119">Header</span></span><br/> | <dl> <span data-ttu-id="876d8-120"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="876d8-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="876d8-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="876d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876d8-122">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="876d8-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





