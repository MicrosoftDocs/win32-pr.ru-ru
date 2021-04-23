---
title: Сообщение ХЕЛПМСГСТРИНГ (Коммдлг. h)
description: Общее диалоговое окно отправляет зарегистрированное сообщение ХЕЛПМСГСТРИНГ в процедуру окна своего окна-владельца, когда пользователь нажимает кнопку "Справка".
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Диалоговые окна сообщения ХЕЛПМСГСТРИНГ
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137454"
---
# <a name="helpmsgstring-message"></a><span data-ttu-id="83a91-104">Сообщение ХЕЛПМСГСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="83a91-104">HELPMSGSTRING message</span></span>

<span data-ttu-id="83a91-105">Общее диалоговое окно отправляет зарегистрированное сообщение **хелпмсгстринг** в процедуру окна своего окна-владельца, когда пользователь нажимает кнопку " **Справка** ".</span><span class="sxs-lookup"><span data-stu-id="83a91-105">A common dialog box sends the **HELPMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Help** button.</span></span>


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a><span data-ttu-id="83a91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83a91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83a91-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83a91-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83a91-108">Маркер общего диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="83a91-108">A handle to the common dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="83a91-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83a91-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83a91-110">Указатель на структуру инициализации для общего диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="83a91-110">A pointer to the initialization structure for the common dialog box.</span></span> <span data-ttu-id="83a91-111">Эта структура может быть структурой [**чусеколор**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) или [**пажесетупдлг**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .</span><span class="sxs-lookup"><span data-stu-id="83a91-111">This structure can be a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) or [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83a91-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83a91-112">Return value</span></span>

<span data-ttu-id="83a91-113">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="83a91-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83a91-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83a91-114">Remarks</span></span>

<span data-ttu-id="83a91-115">Чтобы получить идентификатор сообщения, отправленного диалоговым окном, необходимо указать константу **хелпмсгстринг** в вызове функции [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) .</span><span class="sxs-lookup"><span data-stu-id="83a91-115">You must specify the **HELPMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="83a91-116">При создании диалогового окна используйте элемент **хвндовнер** структуры инициализации, чтобы указать окно для получения сообщений **хелпмсгстринг** .</span><span class="sxs-lookup"><span data-stu-id="83a91-116">When you create the dialog box, use the **hwndOwner** member of the initialization structure to identify the window to receive **HELPMSGSTRING** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="83a91-117">Требования</span><span class="sxs-lookup"><span data-stu-id="83a91-117">Requirements</span></span>



| <span data-ttu-id="83a91-118">Требование</span><span class="sxs-lookup"><span data-stu-id="83a91-118">Requirement</span></span> | <span data-ttu-id="83a91-119">Значение</span><span class="sxs-lookup"><span data-stu-id="83a91-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a91-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83a91-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83a91-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83a91-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="83a91-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83a91-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83a91-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83a91-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83a91-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="83a91-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83a91-125"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83a91-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="83a91-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="83a91-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="83a91-127">**Хелпмсгстрингв** (Юникод) и **хелпмсгстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="83a91-127">**HELPMSGSTRINGW** (Unicode) and **HELPMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="83a91-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83a91-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="83a91-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="83a91-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="83a91-130">**\_Справка CDN**</span><span class="sxs-lookup"><span data-stu-id="83a91-130">**CDN\_HELP**</span></span>](cdn-help.md)
</dt> <dt>

[<span data-ttu-id="83a91-131">**чусеколор**</span><span class="sxs-lookup"><span data-stu-id="83a91-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="83a91-132">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="83a91-132">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="83a91-133">**финдреплаце**</span><span class="sxs-lookup"><span data-stu-id="83a91-133">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="83a91-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="83a91-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="83a91-135">**принтдлг**</span><span class="sxs-lookup"><span data-stu-id="83a91-135">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[<span data-ttu-id="83a91-136">**пажесетупдлг**</span><span class="sxs-lookup"><span data-stu-id="83a91-136">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="83a91-137">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="83a91-137">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="83a91-138">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="83a91-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="83a91-139">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="83a91-139">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

