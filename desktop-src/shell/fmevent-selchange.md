---
description: Отправляется в библиотеку DLL расширения, когда пользователь выбирает имя файла в окне каталога диспетчера файлов или в окне результатов поиска.
title: Сообщение FMEVENT_SELCHANGE (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: 4b05bca54f75bd48b5e710e31c31e5f0f56a2597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539530"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="37971-103">\_Сообщение фмевент селчанже</span><span class="sxs-lookup"><span data-stu-id="37971-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="37971-104">Отправляется в библиотеку DLL расширения, когда пользователь выбирает имя файла в окне каталога диспетчера файлов или в окне результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="37971-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="37971-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="37971-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37971-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37971-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="37971-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="37971-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="37971-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37971-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="37971-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="37971-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37971-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37971-110">Return value</span></span>

<span data-ttu-id="37971-111">Библиотека DLL расширения должна вернуть нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="37971-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="37971-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="37971-112">Remarks</span></span>

<span data-ttu-id="37971-113">Изменения в древовидной части окна каталога не создают это сообщение.</span><span class="sxs-lookup"><span data-stu-id="37971-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="37971-114">Поскольку пользователь может изменить выбор несколько раз, Библиотека DLL расширения должна сразу же возвращаться после обработки этого сообщения, чтобы не замедлит процесс выбора для пользователя.</span><span class="sxs-lookup"><span data-stu-id="37971-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="37971-115">Требования</span><span class="sxs-lookup"><span data-stu-id="37971-115">Requirements</span></span>



| <span data-ttu-id="37971-116">Требование</span><span class="sxs-lookup"><span data-stu-id="37971-116">Requirement</span></span> | <span data-ttu-id="37971-117">Значение</span><span class="sxs-lookup"><span data-stu-id="37971-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37971-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37971-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37971-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="37971-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="37971-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37971-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37971-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="37971-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37971-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="37971-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="37971-123"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="37971-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37971-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37971-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37971-125">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="37971-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




