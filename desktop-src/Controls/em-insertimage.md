---
title: Сообщение EM_INSERTIMAGE (RichEdit. h)
description: Заменяет выделенный BLOB-объект, который отображает изображение.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- Элементы управления Windows для EM_INSERTIMAGE сообщений
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489450"
---
# <a name="em_insertimage-message"></a><span data-ttu-id="92e3f-104">\_Сообщение ИНСЕРТИМАЖЕ EM</span><span class="sxs-lookup"><span data-stu-id="92e3f-104">EM\_INSERTIMAGE message</span></span>

<span data-ttu-id="92e3f-105">Заменяет выделенный BLOB-объект, который отображает изображение.</span><span class="sxs-lookup"><span data-stu-id="92e3f-105">Replaces the selection with a blob that displays an image.</span></span>


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a><span data-ttu-id="92e3f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92e3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e3f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92e3f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92e3f-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="92e3f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="92e3f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92e3f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92e3f-110">Указатель на структуру [**\_ \_ параметров изображения RichEdit**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) , содержащую большой двоичный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="92e3f-110">A pointer to a [**RICHEDIT\_IMAGE\_PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) structure that contains the image blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e3f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92e3f-111">Return value</span></span>

<span data-ttu-id="92e3f-112">\_При успешном выполнении или один из следующих кодов ошибок возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="92e3f-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="92e3f-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="92e3f-113">Return code</span></span>                                                                                    | <span data-ttu-id="92e3f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="92e3f-114">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="92e3f-115"><dt>**Д \_ Не пройден**</dt></span><span class="sxs-lookup"><span data-stu-id="92e3f-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="92e3f-116">Не удается вставить изображение.</span><span class="sxs-lookup"><span data-stu-id="92e3f-116">Cannot insert the image.</span></span> <br/>                          |
| <dl> <span data-ttu-id="92e3f-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="92e3f-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="92e3f-118">Параметр *lParam* имеет значение null или указывает на недопустимое изображение.</span><span class="sxs-lookup"><span data-stu-id="92e3f-118">The *lParam* parameter is NULL or points to an invalid image.</span></span> |
| <dl> <span data-ttu-id="92e3f-119"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="92e3f-119"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="92e3f-120">Недостаточно свободной памяти.</span><span class="sxs-lookup"><span data-stu-id="92e3f-120">Insufficient memory is available.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="92e3f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92e3f-121">Remarks</span></span>

<span data-ttu-id="92e3f-122">Если выделение является точкой вставки, большой двоичный объект изображения вставляется в позицию курсора.</span><span class="sxs-lookup"><span data-stu-id="92e3f-122">If the selection is an insertion point, the image blob is inserted at the insertion point.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e3f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="92e3f-123">Requirements</span></span>



| <span data-ttu-id="92e3f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="92e3f-124">Requirement</span></span> | <span data-ttu-id="92e3f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="92e3f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92e3f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92e3f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="92e3f-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="92e3f-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="92e3f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92e3f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="92e3f-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="92e3f-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92e3f-130">Header</span><span class="sxs-lookup"><span data-stu-id="92e3f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="92e3f-131"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="92e3f-131"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e3f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92e3f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e3f-133">**EM \_ инсерттабле**</span><span class="sxs-lookup"><span data-stu-id="92e3f-133">**EM\_INSERTTABLE**</span></span>](em-inserttable.md)
</dt> </dl>

 

 





