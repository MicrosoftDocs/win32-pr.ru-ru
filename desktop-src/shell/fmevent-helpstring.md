---
description: Отправляется в процедуру DLL расширения диспетчера файлов, когда диспетчеру файлов требуется строка справки для элемента команды меню или панели инструментов.
title: Сообщение FMEVENT_HELPSTRING (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264434"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="506d4-103">\_Сообщение фмевент HELPSTRING</span><span class="sxs-lookup"><span data-stu-id="506d4-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="506d4-104">Отправляется в процедуру DLL расширения диспетчера файлов, когда диспетчеру файлов требуется строка справки для элемента команды меню или панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="506d4-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="506d4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="506d4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="506d4-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="506d4-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="506d4-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="506d4-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="506d4-108">*лпфмшс*</span><span class="sxs-lookup"><span data-stu-id="506d4-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="506d4-109">Адрес структуры [**FMS \_ HELPSTRING**](fms-helpstring.md) , который передает строковые данные справки по командным элементам.</span><span class="sxs-lookup"><span data-stu-id="506d4-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="506d4-110">Структура **FMS \_ HELPSTRING** определяет элемент команды, для которого требуется строка справки, вместе с маркером ее меню.</span><span class="sxs-lookup"><span data-stu-id="506d4-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="506d4-111">Затем приложение записывает соответствующую строку справки в элемент **сзелп** структуры **FMS \_ HELPSTRING** .</span><span class="sxs-lookup"><span data-stu-id="506d4-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="506d4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="506d4-112">Return value</span></span>

<span data-ttu-id="506d4-113">При обработке этого сообщения процедура DLL расширения должна вернуть нуль.</span><span class="sxs-lookup"><span data-stu-id="506d4-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="506d4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="506d4-114">Requirements</span></span>



| <span data-ttu-id="506d4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="506d4-115">Requirement</span></span> | <span data-ttu-id="506d4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="506d4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="506d4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="506d4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="506d4-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="506d4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="506d4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="506d4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="506d4-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="506d4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="506d4-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="506d4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="506d4-122"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="506d4-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="506d4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="506d4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506d4-124">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="506d4-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="506d4-125">**ФМЕВЕНТ \_ хелпменуитем**</span><span class="sxs-lookup"><span data-stu-id="506d4-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




