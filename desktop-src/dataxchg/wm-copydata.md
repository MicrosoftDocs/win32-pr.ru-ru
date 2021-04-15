---
title: Сообщение WM_COPYDATA (Winuser. h)
description: Приложение отправляет \_ сообщение WM COPYDATA для передачи данных в другое приложение.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- Обмен данными с сообщениями WM_COPYDATA
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491070"
---
# <a name="wm_copydata-message"></a><span data-ttu-id="49db5-104">\_Сообщение COPYDATA WM</span><span class="sxs-lookup"><span data-stu-id="49db5-104">WM\_COPYDATA message</span></span>

<span data-ttu-id="49db5-105">Приложение отправляет сообщение **WM \_ COPYDATA** для передачи данных в другое приложение.</span><span class="sxs-lookup"><span data-stu-id="49db5-105">An application sends the **WM\_COPYDATA** message to pass data to another application.</span></span>


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a><span data-ttu-id="49db5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="49db5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49db5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49db5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49db5-108">Маркер окна, который передает данные.</span><span class="sxs-lookup"><span data-stu-id="49db5-108">A handle to the window passing the data.</span></span>

</dd> <dt>

<span data-ttu-id="49db5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49db5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49db5-110">Указатель на структуру [**копидатаструкт**](/windows/win32/api/winuser/ns-winuser-copydatastruct) , содержащую передаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="49db5-110">A pointer to a [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure that contains the data to be passed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49db5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49db5-111">Return value</span></span>

<span data-ttu-id="49db5-112">Если принимающее приложение обрабатывает это сообщение, оно должно возвращать **значение true**; в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="49db5-112">If the receiving application processes this message, it should return **TRUE**; otherwise, it should return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49db5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49db5-113">Remarks</span></span>

<span data-ttu-id="49db5-114">Передаваемые данные не должны содержать указатели или другие ссылки на объекты, недоступные для приложения, получающего данные.</span><span class="sxs-lookup"><span data-stu-id="49db5-114">The data being passed must not contain pointers or other references to objects not accessible to the application receiving the data.</span></span>

<span data-ttu-id="49db5-115">При отправке этого сообщения данные, на которые указывают ссылки, не должны изменяться другим потоком отправляющего процесса.</span><span class="sxs-lookup"><span data-stu-id="49db5-115">While this message is being sent, the referenced data must not be changed by another thread of the sending process.</span></span>

<span data-ttu-id="49db5-116">Принимающее приложение должно учитывать данные, которые доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="49db5-116">The receiving application should consider the data read-only.</span></span> <span data-ttu-id="49db5-117">Параметр *lParam* действителен только во время обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="49db5-117">The *lParam* parameter is valid only during the processing of the message.</span></span> <span data-ttu-id="49db5-118">Принимающее приложение не должно освобождать память, на которую ссылается *lParam*.</span><span class="sxs-lookup"><span data-stu-id="49db5-118">The receiving application should not free the memory referenced by *lParam*.</span></span> <span data-ttu-id="49db5-119">Если принимающее приложение должно получить доступ к данным после возврата [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , оно должно скопировать данные в локальный буфер.</span><span class="sxs-lookup"><span data-stu-id="49db5-119">If the receiving application must access the data after [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, it must copy the data into a local buffer.</span></span>

## <a name="examples"></a><span data-ttu-id="49db5-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="49db5-120">Examples</span></span>

<span data-ttu-id="49db5-121">Пример см. в разделе [Использование копирования данных](using-data-copy.md).</span><span class="sxs-lookup"><span data-stu-id="49db5-121">For an example, see [Using Data Copy](using-data-copy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49db5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="49db5-122">Requirements</span></span>



| <span data-ttu-id="49db5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="49db5-123">Requirement</span></span> | <span data-ttu-id="49db5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="49db5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49db5-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49db5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49db5-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="49db5-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="49db5-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49db5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49db5-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="49db5-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49db5-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="49db5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="49db5-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49db5-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49db5-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49db5-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="49db5-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="49db5-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49db5-133">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="49db5-133">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="49db5-134">**копидатаструкт**</span><span class="sxs-lookup"><span data-stu-id="49db5-134">**COPYDATASTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

