---
title: Сообщение ACM_OPEN (Коммктрл. h)
description: Открывает ролик AVI и отображает его первый кадр в элементе управления анимации. Это сообщение можно отправить явным образом или воспользоваться \_ макросом анимации Open или анимировать \_ опенекс. Мы рекомендуем использовать версию этого сообщения в Юникоде, ACM \_ опенв.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- Элементы управления Windows для ACM_OPEN сообщений
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415005"
---
# <a name="acm_open-message"></a><span data-ttu-id="41293-106">ACM \_ открытое сообщение</span><span class="sxs-lookup"><span data-stu-id="41293-106">ACM\_OPEN message</span></span>

<span data-ttu-id="41293-107">Открывает ролик AVI и отображает его первый кадр в элементе управления анимации.</span><span class="sxs-lookup"><span data-stu-id="41293-107">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="41293-108">Это сообщение можно отправить явным образом или воспользоваться макросом [**анимации \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) или [**анимировать \_ опенекс**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) .</span><span class="sxs-lookup"><span data-stu-id="41293-108">You can send this message explicitly or use the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) or [**Animate\_OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) macro.</span></span> <span data-ttu-id="41293-109">Мы рекомендуем использовать версию этого сообщения в Юникоде, ACM \_ опенв.</span><span class="sxs-lookup"><span data-stu-id="41293-109">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

## <a name="parameters"></a><span data-ttu-id="41293-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="41293-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41293-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41293-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41293-112">[Версия 4,71](common-control-versions.md) и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="41293-112">[Version 4.71](common-control-versions.md) and later.</span></span> <span data-ttu-id="41293-113">Экземпляр обработчика для модуля, из которого должен быть загружен ресурс.</span><span class="sxs-lookup"><span data-stu-id="41293-113">An instance handle to the module from which the resource should be loaded.</span></span> <span data-ttu-id="41293-114">Присвойте этому параметру значение **null** , чтобы элемент управления использовал значение HINSTANCE, используемое для создания окна.</span><span class="sxs-lookup"><span data-stu-id="41293-114">Set this value to **NULL** to have the control use the HINSTANCE value used to create the window.</span></span> <span data-ttu-id="41293-115">Обратите внимание, что если окно создается библиотекой DLL, значение параметра *wParam* по умолчанию — это значение HINSTANCE библиотеки DLL, а не приложение, ВЫЗЫВАЮЩЕЕ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="41293-115">Note that if the window is created by a DLL, the default value for *wParam* is the HINSTANCE value of the DLL, not of the application that calls the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="41293-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41293-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41293-117">Указатель на буфер, содержащий путь к AVI-файлу или имя ресурса AVI.</span><span class="sxs-lookup"><span data-stu-id="41293-117">A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource.</span></span> <span data-ttu-id="41293-118">Кроме того, этот параметр может состоять из идентификатора ресурса AVI в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) и нуль в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41293-118">Alternatively, this parameter can consist of the AVI resource identifier in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and zero in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="41293-119">Чтобы создать это значение, используйте макрос [**макеинтресаурце**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="41293-119">To create this value, use the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="41293-120">Элемент управления загружает ресурс AVI из модуля, указанного в обработчике экземпляра, переданном в функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , в макрос [**анимации \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) или в функцию создания диалогового окна, которая создала элемент управления.</span><span class="sxs-lookup"><span data-stu-id="41293-120">The control loads the AVI resource from the module specified by the instance handle passed to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function, the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro, or the dialog box creation function that created the control.</span></span> <span data-ttu-id="41293-121">В [версии 4,71](common-control-versions.md) и более поздних ресурс загружается из модуля, указанного параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="41293-121">In [Version 4.71](common-control-versions.md) and later, the resource is loaded from the module specified by *wParam*.</span></span> <span data-ttu-id="41293-122">Ресурс AVI должен иметь тип AVI.</span><span class="sxs-lookup"><span data-stu-id="41293-122">An AVI resource must have the "AVI" type.</span></span> <span data-ttu-id="41293-123">Если этот параметр имеет **значение NULL**, система ЗАкрывает AVI-файл, который ранее был открыт для указанного элемента управления анимации, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="41293-123">If this parameter is **NULL**, the system closes the AVI file that was previously opened for the specified animation control, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41293-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41293-124">Return value</span></span>

<span data-ttu-id="41293-125">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="41293-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41293-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41293-126">Remarks</span></span>

<span data-ttu-id="41293-127">Файл AVI или ресурс, указанный параметром *лпсзнаме* , не должен содержать звук.</span><span class="sxs-lookup"><span data-stu-id="41293-127">The AVI file or resource specified by *lpszName* must not contain audio.</span></span>

<span data-ttu-id="41293-128">Мы рекомендуем использовать версию этого сообщения в Юникоде, ACM \_ опенв.</span><span class="sxs-lookup"><span data-stu-id="41293-128">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

<span data-ttu-id="41293-129">Вы можете открывать только оповещения AVI.</span><span class="sxs-lookup"><span data-stu-id="41293-129">You can only open silent AVI clips.</span></span> <span data-ttu-id="41293-130">ACM \_ Open и [**анимировать \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) Fail, если свойство *lParam* задает ролик AVI, содержащий звук.</span><span class="sxs-lookup"><span data-stu-id="41293-130">ACM\_OPEN and [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) fail if *lParam* specifies an AVI clip that contains sound.</span></span>

<span data-ttu-id="41293-131">Для закрытия файла AVI или ресурса AVI, который был ранее открыт для указанного элемента управления анимацией, можно использовать параметр [**анимировать \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) .</span><span class="sxs-lookup"><span data-stu-id="41293-131">You can use [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) to close an AVI file or AVI resource that was previously opened for the specified animation control.</span></span>

## <a name="requirements"></a><span data-ttu-id="41293-132">Требования</span><span class="sxs-lookup"><span data-stu-id="41293-132">Requirements</span></span>



| <span data-ttu-id="41293-133">Требование</span><span class="sxs-lookup"><span data-stu-id="41293-133">Requirement</span></span> | <span data-ttu-id="41293-134">Значение</span><span class="sxs-lookup"><span data-stu-id="41293-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41293-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41293-135">Minimum supported client</span></span><br/> | <span data-ttu-id="41293-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41293-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41293-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41293-137">Minimum supported server</span></span><br/> | <span data-ttu-id="41293-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41293-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41293-139">Header</span><span class="sxs-lookup"><span data-stu-id="41293-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="41293-140"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="41293-140"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="41293-141">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="41293-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41293-142">**ACM \_ ОПЕНВ** (Юникод) и **ACM \_ Open** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="41293-142">**ACM\_OPENW** (Unicode) and **ACM\_OPENA** (ANSI)</span></span><br/>                         |



 

