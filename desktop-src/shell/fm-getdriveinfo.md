---
description: Отправляется расширением диспетчера файлов для получения сведений о диске из активного окна диспетчера файлов.
title: Сообщение FM_GETDRIVEINFO (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997219"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="cdbed-103">\_Сообщение FM жетдривеинфо</span><span class="sxs-lookup"><span data-stu-id="cdbed-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="cdbed-104">Отправляется расширением диспетчера файлов для получения сведений о диске из активного окна диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="cdbed-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdbed-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdbed-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdbed-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdbed-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cdbed-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cdbed-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cdbed-108">*лпфмсгди*</span><span class="sxs-lookup"><span data-stu-id="cdbed-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="cdbed-109">Адрес структуры [**FMS \_ жетдривеинфо**](fms-getdriveinfo.md) , которая получает сведения о диске.</span><span class="sxs-lookup"><span data-stu-id="cdbed-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdbed-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdbed-110">Return value</span></span>

<span data-ttu-id="cdbed-111">Возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="cdbed-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdbed-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="cdbed-112">Remarks</span></span>

<span data-ttu-id="cdbed-113">Если значение 0xFFFFFFFF возвращается в члене **двтоталспаце** или **двфриспаце** структуры [**FMS \_ жетдривеинфо**](fms-getdriveinfo.md) , то библиотека расширений должна вычислять значения или значения.</span><span class="sxs-lookup"><span data-stu-id="cdbed-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdbed-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cdbed-114">Requirements</span></span>



| <span data-ttu-id="cdbed-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cdbed-115">Requirement</span></span> | <span data-ttu-id="cdbed-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cdbed-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cdbed-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdbed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cdbed-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdbed-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cdbed-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdbed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cdbed-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdbed-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cdbed-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cdbed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdbed-122"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdbed-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdbed-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdbed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdbed-124">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="cdbed-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




