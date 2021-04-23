---
title: Сообщение СЕТРГБСТРИНГ (Коммдлг. h)
description: Процедура-обработчик диалогового окна цвета, Кчукпрок, может отправить в диалоговое окно зарегистрированное сообщение СЕТРГБСТРИНГ, чтобы задать текущее выделение цветом.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Диалоговые окна сообщения СЕТРГБСТРИНГ
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803089"
---
# <a name="setrgbstring-message"></a><span data-ttu-id="ad0ea-104">Сообщение СЕТРГБСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="ad0ea-104">SETRGBSTRING message</span></span>

<span data-ttu-id="ad0ea-105">Процедура-обработчик диалогового окна **цвета** , [*кчукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), может отправить в диалоговое окно зарегистрированное сообщение **сетргбстринг** , чтобы задать текущее выделение цветом.</span><span class="sxs-lookup"><span data-stu-id="ad0ea-105">The hook procedure of a **Color** dialog box, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), can send the **SETRGBSTRING** registered message to the dialog box to set the current color selection.</span></span>


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a><span data-ttu-id="ad0ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad0ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad0ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad0ea-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad0ea-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="ad0ea-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad0ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad0ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad0ea-110">Значение RGB цвета, которое необходимо выбрать в диалоговом окне " **Цвет** ".</span><span class="sxs-lookup"><span data-stu-id="ad0ea-110">The RGB value of the color to select in the **Color** dialog box.</span></span> <span data-ttu-id="ad0ea-111">С помощью макроса [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) можно задать красный, зеленый и синий интенситиес в значении цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="ad0ea-111">You can use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro to specify the red, green, and blue intensities of an RGB color value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad0ea-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad0ea-112">Return value</span></span>

<span data-ttu-id="ad0ea-113">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ad0ea-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad0ea-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad0ea-114">Remarks</span></span>

<span data-ttu-id="ad0ea-115">Если параметр *lParam* соответствует одному из основных цветов или одному из 16 пользовательских цветов, то процедура выбора этого цвета выбирается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ad0ea-115">If *lParam* matches one of the basic colors or one of the 16 custom colors, the dialog box procedure selects that color.</span></span> <span data-ttu-id="ad0ea-116">Процедура также обновляет все элементы управления в пользовательском расширении цвета диалогового окна **Цвет** , если оно открыто.</span><span class="sxs-lookup"><span data-stu-id="ad0ea-116">The dialog box procedure also updates all the controls in the custom color extension of the **Color** dialog box, if it is open.</span></span>

<span data-ttu-id="ad0ea-117">Если параметр *lParam* не соответствует базовому или пользовательскому цвету, то процедура диалогового окна не изменяет текущий выбор цвета, но обновляет элементы управления пользовательского цвета, если они видимы.</span><span class="sxs-lookup"><span data-stu-id="ad0ea-117">If *lParam* does not match a basic or custom color, the dialog box procedure does not change the current color selection, but it does update the custom color controls, if they are visible.</span></span>

## <a name="examples"></a><span data-ttu-id="ad0ea-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="ad0ea-118">Examples</span></span>

<span data-ttu-id="ad0ea-119">В следующем примере кода возвращается идентификатор сообщения **сетргбстринг** , а затем выбирается синий цвет.</span><span class="sxs-lookup"><span data-stu-id="ad0ea-119">The following sample code gets the **SETRGBSTRING** message identifier and then sets the color selection to blue.</span></span>


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a><span data-ttu-id="ad0ea-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ad0ea-120">Requirements</span></span>



| <span data-ttu-id="ad0ea-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ad0ea-121">Requirement</span></span> | <span data-ttu-id="ad0ea-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ad0ea-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0ea-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad0ea-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ad0ea-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad0ea-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad0ea-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad0ea-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ad0ea-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad0ea-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad0ea-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ad0ea-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad0ea-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad0ea-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ad0ea-129">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="ad0ea-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ad0ea-130">**Сетргбстрингв** (Юникод) и **сетргбстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ad0ea-130">**SETRGBSTRINGW** (Unicode) and **SETRGBSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="ad0ea-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad0ea-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad0ea-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ad0ea-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad0ea-133">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="ad0ea-133">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="ad0ea-134">**RGB**</span><span class="sxs-lookup"><span data-stu-id="ad0ea-134">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[<span data-ttu-id="ad0ea-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="ad0ea-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

<span data-ttu-id="ad0ea-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ad0ea-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ad0ea-137">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="ad0ea-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

