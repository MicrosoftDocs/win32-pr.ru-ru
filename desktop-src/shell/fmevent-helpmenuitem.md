---
description: Отправляется в процедуру DLL расширения диспетчера файлов, когда пользователь нажимает клавишу F1 в меню или элементе команды панели инструментов. Расширение должно вызывать WinHelp, а параметр HWND этой функции имеет значение, равное значению параметра HWND расширения.
title: Сообщение FMEVENT_HELPMENUITEM (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984205"
---
# <a name="fmevent_helpmenuitem-message"></a><span data-ttu-id="fc3cc-104">\_Сообщение фмевент хелпменуитем</span><span class="sxs-lookup"><span data-stu-id="fc3cc-104">FMEVENT\_HELPMENUITEM message</span></span>

<span data-ttu-id="fc3cc-105">Отправляется в процедуру DLL расширения диспетчера файлов, когда пользователь нажимает клавишу F1 в меню или элементе команды панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-105">Sent to a File Manager extension DLL procedure when the user presses F1 on a menu or toolbar command item.</span></span> <span data-ttu-id="fc3cc-106">Расширение должно вызывать [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), а параметр *HWND* этой функции имеет значение, равное значению параметра *HWND* расширения.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-106">The extension should call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), with that function's *hwnd* parameter set to the value of the extension's *hwnd* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc3cc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc3cc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc3cc-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc3cc-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fc3cc-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fc3cc-110">*уитем*</span><span class="sxs-lookup"><span data-stu-id="fc3cc-110">*uItem*</span></span> 
</dt> <dd>

<span data-ttu-id="fc3cc-111">Значение, идентифицирующее элемент команды меню или панели инструментов, для которого требуется справка.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-111">A value that identifies the menu or toolbar command item for which Help is desired.</span></span> <span data-ttu-id="fc3cc-112">Процедура расширения использует это значение для определения наилучшего вызова [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span><span class="sxs-lookup"><span data-stu-id="fc3cc-112">The extension procedure uses this value to determine how best to call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc3cc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc3cc-113">Return value</span></span>

<span data-ttu-id="fc3cc-114">При обработке этого сообщения процедура DLL расширения должна вернуть нуль.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-114">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc3cc-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fc3cc-115">Requirements</span></span>



| <span data-ttu-id="fc3cc-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fc3cc-116">Requirement</span></span> | <span data-ttu-id="fc3cc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fc3cc-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3cc-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc3cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc3cc-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc3cc-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fc3cc-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc3cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc3cc-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc3cc-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fc3cc-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fc3cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc3cc-123"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc3cc-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc3cc-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc3cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3cc-125">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="fc3cc-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="fc3cc-126">**ФМЕВЕНТ \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="fc3cc-126">**FMEVENT\_HELPSTRING**</span></span>](fmevent-helpstring.md)
</dt> </dl>

 

 




