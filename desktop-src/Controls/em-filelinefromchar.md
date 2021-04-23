---
title: Сообщение EM_FILELINEFROMCHAR (Коммктрл. h)
description: Возвращает индекс строки, содержащей указанный индекс символа в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Элементы управления Windows для EM_FILELINEFROMCHAR сообщений
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491223"
---
# <a name="em_filelinefromchar-message"></a><span data-ttu-id="cb54e-104">\_Сообщение ФИЛЕЛИНЕФРОМЧАР EM</span><span class="sxs-lookup"><span data-stu-id="cb54e-104">EM\_FILELINEFROMCHAR message</span></span>

<span data-ttu-id="cb54e-105">Возвращает индекс строки, содержащей указанный индекс символа в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="cb54e-105">Gets the index of the line that contains the specified character index in a multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="cb54e-106">Индекс символа — это Отсчитываемый от нуля индекс символа, начиная с начала элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="cb54e-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb54e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb54e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb54e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb54e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb54e-109">Индекс символа, содержащегося в строке, номер которой должен быть получен.</span><span class="sxs-lookup"><span data-stu-id="cb54e-109">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="cb54e-110">Если этот параметр имеет значение-1, **EM \_ филелинефромчар** получает номер строки текущей строки (строка, содержащая курсор) или, если имеется выделенный фрагмент, номер строки, содержащей начало выделения.</span><span class="sxs-lookup"><span data-stu-id="cb54e-110">If this parameter is -1, **EM\_FILELINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="cb54e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb54e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb54e-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="cb54e-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb54e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb54e-113">Return value</span></span>

<span data-ttu-id="cb54e-114">Возвращаемое значение — это номер строки (начинающийся с нуля) строки, содержащей индекс символа, заданный параметром *wParam*, независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="cb54e-114">The return value is the zero-based line number of the line containing the character index specified by *wParam*, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb54e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cb54e-115">Requirements</span></span>



| <span data-ttu-id="cb54e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cb54e-116">Requirement</span></span> | <span data-ttu-id="cb54e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cb54e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb54e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb54e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb54e-119">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="cb54e-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb54e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb54e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb54e-121">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="cb54e-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb54e-122">Header</span><span class="sxs-lookup"><span data-stu-id="cb54e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb54e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb54e-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb54e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb54e-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb54e-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="cb54e-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb54e-126">**EM \_ филелинеиндекс**</span><span class="sxs-lookup"><span data-stu-id="cb54e-126">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





