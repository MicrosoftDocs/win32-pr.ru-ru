---
title: Сообщение TB_ADDBITMAP (Коммктрл. h)
description: Добавляет одно или несколько изображений в список изображений кнопок, доступных для панели инструментов.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- Элементы управления Windows для TB_ADDBITMAP сообщений
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804127"
---
# <a name="tb_addbitmap-message"></a><span data-ttu-id="af1a0-104">\_Сообщение АДДБИТМАП ТБ</span><span class="sxs-lookup"><span data-stu-id="af1a0-104">TB\_ADDBITMAP message</span></span>

<span data-ttu-id="af1a0-105">Добавляет одно или несколько изображений в список изображений кнопок, доступных для панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="af1a0-105">Adds one or more images to the list of button images available for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="af1a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af1a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af1a0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af1a0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af1a0-108">Число изображений кнопок в точечном рисунке.</span><span class="sxs-lookup"><span data-stu-id="af1a0-108">Number of button images in the bitmap.</span></span> <span data-ttu-id="af1a0-109">Если аргумент *lParam* задает системный точечный рисунок, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="af1a0-109">If *lParam* specifies a system-defined bitmap, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="af1a0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af1a0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af1a0-111">Указатель на структуру [**тбаддбитмап**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) , которая содержит идентификатор ресурса точечного рисунка и маркер для экземпляра модуля с исполняемым файлом, содержащим ресурс точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="af1a0-111">Pointer to a [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) structure that contains the identifier of a bitmap resource and the handle to the module instance with the executable file that contains the bitmap resource.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af1a0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af1a0-112">Return value</span></span>

<span data-ttu-id="af1a0-113">Возвращает индекс первого нового изображения, если выполнено успешно, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="af1a0-113">Returns the index of the first new image if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af1a0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af1a0-114">Remarks</span></span>

<span data-ttu-id="af1a0-115">Если панель инструментов была создана с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , перед отправкой **\_ аддбитмап ТБ** необходимо отправить на панель инструментов сообщение [**\_ буттонструктсизе**](tb-buttonstructsize.md) ТБ.</span><span class="sxs-lookup"><span data-stu-id="af1a0-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBITMAP**.</span></span>

## <a name="examples"></a><span data-ttu-id="af1a0-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="af1a0-116">Examples</span></span>

<span data-ttu-id="af1a0-117">В следующем примере создается точечный рисунок из ресурса (IDB \_ BITMAP1), который сопоставляет цвет фона (черный в данном случае) с цветом лицевой кнопки системы и добавляет его на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="af1a0-117">The following example creates a bitmap from a resource (IDB\_BITMAP1), maps the background color (black in this case) to the system button face color, and adds it to the toolbar.</span></span>


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a><span data-ttu-id="af1a0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="af1a0-118">Requirements</span></span>



| <span data-ttu-id="af1a0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="af1a0-119">Requirement</span></span> | <span data-ttu-id="af1a0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="af1a0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af1a0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af1a0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="af1a0-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af1a0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af1a0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af1a0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="af1a0-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af1a0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af1a0-125">Header</span><span class="sxs-lookup"><span data-stu-id="af1a0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="af1a0-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="af1a0-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

