---
title: Сообщение TB_SETBUTTONSIZE (Коммктрл. h)
description: Задает размер кнопок на панели инструментов.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- Элементы управления Windows для TB_SETBUTTONSIZE сообщений
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654518"
---
# <a name="tb_setbuttonsize-message"></a><span data-ttu-id="7e387-104">\_Сообщение СЕТБУТТОНСИЗЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="7e387-104">TB\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="7e387-105">Задает размер кнопок на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="7e387-105">Sets the size of buttons on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e387-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e387-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e387-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e387-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e387-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7e387-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7e387-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e387-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e387-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает ширину (в пикселях) кнопок.</span><span class="sxs-lookup"><span data-stu-id="7e387-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the buttons.</span></span> <span data-ttu-id="7e387-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает высоту кнопок в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7e387-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e387-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e387-112">Return value</span></span>

<span data-ttu-id="7e387-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7e387-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e387-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e387-114">Remarks</span></span>

<span data-ttu-id="7e387-115">**ТБ \_ СЕТБУТТОНСИЗЕ** обычно следует вызывать после добавления кнопок.</span><span class="sxs-lookup"><span data-stu-id="7e387-115">**TB\_SETBUTTONSIZE** should generally be called after adding buttons.</span></span>

<span data-ttu-id="7e387-116">Используйте [**ТБ \_ сетбуттонвидс**](tb-setbuttonwidth.md) , чтобы задать максимальную и минимальную допустимую ширину для кнопок перед их добавлением.</span><span class="sxs-lookup"><span data-stu-id="7e387-116">Use [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="7e387-117">Чтобы задать фактический размер кнопок, используйте **\_ сетбуттонсизе ТБ** .</span><span class="sxs-lookup"><span data-stu-id="7e387-117">Use **TB\_SETBUTTONSIZE** to set the actual size of buttons.</span></span>

## <a name="examples"></a><span data-ttu-id="7e387-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="7e387-118">Examples</span></span>

<span data-ttu-id="7e387-119">В следующем примере кода устанавливается ширина кнопок 80 пикселей, а высота — 30 пикселей.</span><span class="sxs-lookup"><span data-stu-id="7e387-119">The following example code sets the width of buttons to 80 pixels and the height to 30 pixels.</span></span>


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a><span data-ttu-id="7e387-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7e387-120">Requirements</span></span>



| <span data-ttu-id="7e387-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7e387-121">Requirement</span></span> | <span data-ttu-id="7e387-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7e387-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e387-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e387-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7e387-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e387-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e387-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e387-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7e387-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e387-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e387-127">Header</span><span class="sxs-lookup"><span data-stu-id="7e387-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e387-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e387-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

