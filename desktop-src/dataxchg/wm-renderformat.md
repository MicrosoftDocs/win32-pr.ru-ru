---
title: Сообщение WM_RENDERFORMAT (Winuser. h)
description: Отправляется владельцу буфера обмена, если он имеет отложенную визуализацию определенного формата буфера обмена и если приложение запрашивает данные в этом формате.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- Обмен данными с сообщениями WM_RENDERFORMAT
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340710"
---
# <a name="wm_renderformat-message"></a><span data-ttu-id="c8d06-104">\_Сообщение RENDERFORMAT WM</span><span class="sxs-lookup"><span data-stu-id="c8d06-104">WM\_RENDERFORMAT message</span></span>

<span data-ttu-id="c8d06-105">Отправляется владельцу буфера обмена, если он имеет отложенную визуализацию определенного формата буфера обмена и если приложение запрашивает данные в этом формате.</span><span class="sxs-lookup"><span data-stu-id="c8d06-105">Sent to the clipboard owner if it has delayed rendering a specific clipboard format and if an application has requested data in that format.</span></span> <span data-ttu-id="c8d06-106">Владелец буфера обмена должен визуализировать данные в указанном формате и поместить их в буфер обмена, вызвав функцию [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="c8d06-106">The clipboard owner must render data in the specified format and place it on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a><span data-ttu-id="c8d06-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8d06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d06-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8d06-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8d06-109">[Формат буфера обмена](standard-clipboard-formats.md) для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="c8d06-109">The [clipboard format](standard-clipboard-formats.md) to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="c8d06-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8d06-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8d06-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c8d06-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8d06-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8d06-112">Return value</span></span>

<span data-ttu-id="c8d06-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="c8d06-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8d06-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8d06-114">Remarks</span></span>

<span data-ttu-id="c8d06-115">При ответе на сообщение **WM \_ RENDERFORMAT** владелец буфера обмена не должен открывать буфер обмена перед вызовом [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="c8d06-115">When responding to a **WM\_RENDERFORMAT** message, the clipboard owner must not open the clipboard before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span> <span data-ttu-id="c8d06-116">Открытие буфера обмена не является обязательным, прежде чем поместить данные в ответ на **WM \_ RENDERFORMAT**, и любая попытка открыть буфер обмена завершится ошибкой, так как буфер обмена в настоящий момент остается открытым приложением, которое запросило отправку формата.</span><span class="sxs-lookup"><span data-stu-id="c8d06-116">Opening the clipboard is not necessary before placing data in response to **WM\_RENDERFORMAT**, and any attempt to open the clipboard will fail because the clipboard is currently being held open by the application that requested the format to be rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8d06-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c8d06-117">Requirements</span></span>



| <span data-ttu-id="c8d06-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c8d06-118">Requirement</span></span> | <span data-ttu-id="c8d06-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c8d06-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d06-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8d06-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c8d06-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c8d06-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c8d06-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8d06-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c8d06-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c8d06-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8d06-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c8d06-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8d06-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8d06-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8d06-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8d06-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8d06-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c8d06-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8d06-128">**сетклипбоарддата**</span><span class="sxs-lookup"><span data-stu-id="c8d06-128">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="c8d06-129">**WM \_ рендераллформатс**</span><span class="sxs-lookup"><span data-stu-id="c8d06-129">**WM\_RENDERALLFORMATS**</span></span>](wm-renderallformats.md)
</dt> <dt>

<span data-ttu-id="c8d06-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="c8d06-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8d06-131">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="c8d06-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

 





