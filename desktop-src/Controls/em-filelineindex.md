---
title: Сообщение EM_FILELINEINDEX (Коммктрл. h)
description: Возвращает символьный индекс первого символа указанной строки в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Элементы управления Windows для EM_FILELINEINDEX сообщений
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136263"
---
# <a name="em_filelineindex-message-commctrlh"></a><span data-ttu-id="71b57-104">Сообщение EM_FILELINEINDEX (Коммктрл. h)</span><span class="sxs-lookup"><span data-stu-id="71b57-104">EM_FILELINEINDEX message (CommCtrl.h)</span></span>

<span data-ttu-id="71b57-105">Возвращает символьный индекс первого символа указанной строки в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="71b57-105">Gets the character index of the first character of a specified line in a multiline edit control, independently of how lines are displayed on the screen..</span></span> <span data-ttu-id="71b57-106">Индекс символа — это Отсчитываемый от нуля индекс символа, начиная с начала элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="71b57-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="71b57-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="71b57-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b57-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71b57-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71b57-109">Номер строки, начинающейся с нуля.</span><span class="sxs-lookup"><span data-stu-id="71b57-109">The zero-based line number.</span></span> <span data-ttu-id="71b57-110">Значение-1 указывает текущий номер строки (строка, содержащая курсор).</span><span class="sxs-lookup"><span data-stu-id="71b57-110">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="71b57-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71b57-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71b57-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="71b57-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b57-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71b57-113">Return value</span></span>

<span data-ttu-id="71b57-114">Возвращаемое значение — это индекс символа строки, указанной в параметре *wParam* , независимо от того, как линии отображаются на экране, или-1, если номер строки больше числа строк в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="71b57-114">The return value is the character index of the line specified in the *wParam* parameter, independently of how lines are displayed on the screen, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b57-115">Требования</span><span class="sxs-lookup"><span data-stu-id="71b57-115">Requirements</span></span>



| <span data-ttu-id="71b57-116">Требование</span><span class="sxs-lookup"><span data-stu-id="71b57-116">Requirement</span></span> | <span data-ttu-id="71b57-117">Значение</span><span class="sxs-lookup"><span data-stu-id="71b57-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b57-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71b57-118">Minimum supported client</span></span><br/> | <span data-ttu-id="71b57-119">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="71b57-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71b57-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71b57-120">Minimum supported server</span></span><br/> | <span data-ttu-id="71b57-121">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="71b57-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71b57-122">Header</span><span class="sxs-lookup"><span data-stu-id="71b57-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b57-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b57-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b57-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71b57-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b57-125">**EM \_ филелинефромчар**</span><span class="sxs-lookup"><span data-stu-id="71b57-125">**EM\_FILELINEFROMCHAR**</span></span>](em-filelinefromchar.md)
</dt> </dl>

 

 





