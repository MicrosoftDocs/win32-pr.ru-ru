---
description: Отправляется в самое верхнее окно после изменения языка ввода приложения. Необходимо внести все зависящие от приложения параметры и передать сообщение функции Дефвиндовпрок, которая передает сообщение всем дочерним окнам первого уровня.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Сообщение WM_INPUTLANGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332409"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="ec4e8-104">\_Сообщение ИНПУТЛАНГЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="ec4e8-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="ec4e8-105">Отправляется в самое верхнее окно после изменения языка ввода приложения.</span><span class="sxs-lookup"><span data-stu-id="ec4e8-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="ec4e8-106">Необходимо внести все зависящие от приложения параметры и передать сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , которая передает сообщение всем дочерним окнам первого уровня.</span><span class="sxs-lookup"><span data-stu-id="ec4e8-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="ec4e8-107">Эти дочерние окна могут передать сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , чтобы оно передавало сообщение дочерним окнам и так далее.</span><span class="sxs-lookup"><span data-stu-id="ec4e8-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="ec4e8-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ec4e8-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a><span data-ttu-id="ec4e8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec4e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec4e8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec4e8-110">*wParam*</span></span>

</dt> <dd>
  
<span data-ttu-id="ec4e8-111">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="ec4e8-111">Type: **WPARAM**</span></span>

<span data-ttu-id="ec4e8-112">[Кодовая страница](../Intl/code-pages.md) нового языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="ec4e8-112">The [code page](../Intl/code-pages.md) of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="ec4e8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec4e8-113">*lParam*</span></span>

</dt> <dd>
 
<span data-ttu-id="ec4e8-114">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="ec4e8-114">Type: **LPARAM**</span></span>

<span data-ttu-id="ec4e8-115">Идентификатор языка ввода **HKL** .</span><span class="sxs-lookup"><span data-stu-id="ec4e8-115">The **HKL** input locale identifier.</span></span> <span data-ttu-id="ec4e8-116">Дополнительные сведения см. в разделе [языки, языковые стандарты и раскладки клавиатуры](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="ec4e8-116">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec4e8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec4e8-117">Return value</span></span>

<span data-ttu-id="ec4e8-118">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="ec4e8-118">Type: **LRESULT**</span></span>

<span data-ttu-id="ec4e8-119">Приложение должно вернуть ненулевое значение, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="ec4e8-119">An application should return nonzero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec4e8-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec4e8-120">Remarks</span></span>

<span data-ttu-id="ec4e8-121">Вы можете получить [имя локали](../Intl/locale-names.md) клавиатуры с помощью функции [лЦидтолокаленаме](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) .</span><span class="sxs-lookup"><span data-stu-id="ec4e8-121">You can retrieve keyboard [locale name](../Intl/locale-names.md) via [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) function.</span></span> <span data-ttu-id="ec4e8-122">С помощью имени языкового стандарта можно использовать [современные функции языкового стандарта](/windows/win32/intl/calling-the--locale-name--functions):</span><span class="sxs-lookup"><span data-stu-id="ec4e8-122">With locale name you can use [modern locale functions](/windows/win32/intl/calling-the--locale-name--functions):</span></span>

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a><span data-ttu-id="ec4e8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ec4e8-123">Requirements</span></span>

| <span data-ttu-id="ec4e8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ec4e8-124">Requirement</span></span> | <span data-ttu-id="ec4e8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4e8-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec4e8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec4e8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ec4e8-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec4e8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ec4e8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec4e8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ec4e8-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec4e8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ec4e8-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ec4e8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec4e8-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec4e8-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ec4e8-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec4e8-132">See also</span></span>

<span data-ttu-id="ec4e8-133">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="ec4e8-133">**Reference**</span></span>

- [<span data-ttu-id="ec4e8-134">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="ec4e8-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [<span data-ttu-id="ec4e8-135">**WM \_ инпутлангчанжерекуест**</span><span class="sxs-lookup"><span data-stu-id="ec4e8-135">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)

<span data-ttu-id="ec4e8-136">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="ec4e8-136">**Conceptual**</span></span>

- [<span data-ttu-id="ec4e8-137">Windows</span><span class="sxs-lookup"><span data-stu-id="ec4e8-137">Windows</span></span>](windows.md) 
