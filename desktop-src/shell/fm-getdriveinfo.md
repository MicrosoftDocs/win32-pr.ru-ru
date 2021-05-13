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
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842415"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="58437-103">\_Сообщение FM жетдривеинфо</span><span class="sxs-lookup"><span data-stu-id="58437-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="58437-104">Отправляется расширением диспетчера файлов для получения сведений о диске из активного окна диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="58437-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="58437-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="58437-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58437-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58437-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="58437-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="58437-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="58437-108">*лпфмсгди*</span><span class="sxs-lookup"><span data-stu-id="58437-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="58437-109">Адрес структуры [**FMS \_ жетдривеинфо**](fms-getdriveinfo.md) , которая получает сведения о диске.</span><span class="sxs-lookup"><span data-stu-id="58437-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58437-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58437-110">Return value</span></span>

<span data-ttu-id="58437-111">Возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="58437-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="58437-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="58437-112">Remarks</span></span>

<span data-ttu-id="58437-113">Если значение 0xFFFFFFFF возвращается в члене **двтоталспаце** или **двфриспаце** структуры [**FMS \_ жетдривеинфо**](fms-getdriveinfo.md) , то библиотека расширений должна вычислять значения или значения.</span><span class="sxs-lookup"><span data-stu-id="58437-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="58437-114">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="58437-114">Requirements</span></span>



| <span data-ttu-id="58437-115">Требование</span><span class="sxs-lookup"><span data-stu-id="58437-115">Requirement</span></span> | <span data-ttu-id="58437-116">Значение</span><span class="sxs-lookup"><span data-stu-id="58437-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58437-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58437-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58437-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="58437-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="58437-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58437-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58437-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="58437-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="58437-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="58437-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="58437-122"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="58437-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58437-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58437-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58437-124">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="58437-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




