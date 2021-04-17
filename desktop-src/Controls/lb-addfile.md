---
title: Сообщение LB_ADDFILE (Winuser. h)
description: Добавляет указанное имя файла в список, содержащий список каталогов.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- Элементы управления Windows для LB_ADDFILE сообщений
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492153"
---
# <a name="lb_addfile-message"></a><span data-ttu-id="ccbce-104">Сообщение ADDFILE балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="ccbce-104">LB\_ADDFILE message</span></span>

<span data-ttu-id="ccbce-105">Добавляет указанное имя файла в список, содержащий список каталогов.</span><span class="sxs-lookup"><span data-stu-id="ccbce-105">Adds the specified filename to a list box that contains a directory listing.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccbce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccbce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccbce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccbce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccbce-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="ccbce-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ccbce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccbce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccbce-110">Указатель на буфер, указывающий имя добавляемого файла.</span><span class="sxs-lookup"><span data-stu-id="ccbce-110">A pointer to a buffer that specifies the name of the file to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccbce-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccbce-111">Return value</span></span>

<span data-ttu-id="ccbce-112">Возвращаемое значение — это Отсчитываемый от нуля индекс добавленного файла или \_ при возникновении ошибки в процессе балансировки нагрузки Err.</span><span class="sxs-lookup"><span data-stu-id="ccbce-112">The return value is the zero-based index of the file that was added, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccbce-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccbce-113">Remarks</span></span>

<span data-ttu-id="ccbce-114">Список, к которому добавляется *lParam* , должен быть заполнен функцией [**длгдирлист**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) .</span><span class="sxs-lookup"><span data-stu-id="ccbce-114">The list box to which *lParam* is added must have been filled by the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function.</span></span>

<span data-ttu-id="ccbce-115">Сообщение [**\_ инитстораже балансировки нагрузки**](lb-initstorage.md) помогает ускорить инициализацию списков с большим количеством элементов (более 100).</span><span class="sxs-lookup"><span data-stu-id="ccbce-115">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="ccbce-116">Он резервирует указанный объем памяти, чтобы последующие сообщения **\_ ADDFILEи балансировки нагрузки** занимали кратчайшее время.</span><span class="sxs-lookup"><span data-stu-id="ccbce-116">It reserves the specified amount of memory so that subsequent **LB\_ADDFILE** messages take the shortest possible time.</span></span> <span data-ttu-id="ccbce-117">Для параметров *wParam* и *lParam* можно использовать оценки.</span><span class="sxs-lookup"><span data-stu-id="ccbce-117">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="ccbce-118">При чрезмерной оценке выделяется дополнительный объем памяти. Если недооценивать, то для элементов, превышающих запрошенный объем, используется нормальное выделение.</span><span class="sxs-lookup"><span data-stu-id="ccbce-118">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="ccbce-119">Для приложения ANSI система преобразует текст в поле со списком в Юникод с помощью команды CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="ccbce-119">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="ccbce-120">Это может вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="ccbce-120">This can cause problems.</span></span> <span data-ttu-id="ccbce-121">Например, римские символы с диакритическими знаками в списке не в Юникоде в японских окнах будут выступать из искажений.</span><span class="sxs-lookup"><span data-stu-id="ccbce-121">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="ccbce-122">Чтобы устранить эту проблему, либо скомпилируйте приложение как Юникод, либо используйте список, рисуемый владельцем.</span><span class="sxs-lookup"><span data-stu-id="ccbce-122">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccbce-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ccbce-123">Requirements</span></span>



| <span data-ttu-id="ccbce-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ccbce-124">Requirement</span></span> | <span data-ttu-id="ccbce-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ccbce-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccbce-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccbce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ccbce-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccbce-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ccbce-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccbce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ccbce-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ccbce-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ccbce-130">Header</span><span class="sxs-lookup"><span data-stu-id="ccbce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccbce-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccbce-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccbce-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccbce-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="ccbce-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ccbce-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ccbce-134">**длгдирлист**</span><span class="sxs-lookup"><span data-stu-id="ccbce-134">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[<span data-ttu-id="ccbce-135">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="ccbce-135">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> </dl>

 

 





