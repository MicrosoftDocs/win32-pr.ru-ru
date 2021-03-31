---
title: Сообщение EM_SETUIANAME (RichEdit. h)
description: Задает имя элемента управления расширенным редактированием для модели автоматизации пользовательского интерфейса (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- Элементы управления Windows для EM_SETUIANAME сообщений
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988821"
---
# <a name="em_setuianame-message"></a><span data-ttu-id="a181b-104">\_Сообщение СЕТУИАНАМЕ EM</span><span class="sxs-lookup"><span data-stu-id="a181b-104">EM\_SETUIANAME message</span></span>

<span data-ttu-id="a181b-105">Задает имя элемента управления расширенным редактированием для модели автоматизации пользовательского интерфейса (UIA).</span><span class="sxs-lookup"><span data-stu-id="a181b-105">Sets the name of a rich edit control for UI Automation (UIA).</span></span>


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a><span data-ttu-id="a181b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a181b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a181b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a181b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a181b-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a181b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a181b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a181b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a181b-110">Указатель на строку имени, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="a181b-110">A pointer to the null-terminated name string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a181b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a181b-111">Return value</span></span>

<span data-ttu-id="a181b-112">Значение TRUE, если имя для UIA успешно установлено; в противном случае — значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="a181b-112">TRUE if the name for UIA is successfully set, otherwise FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a181b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a181b-113">Requirements</span></span>



| <span data-ttu-id="a181b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a181b-114">Requirement</span></span> | <span data-ttu-id="a181b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a181b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a181b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a181b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a181b-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a181b-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a181b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a181b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a181b-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a181b-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a181b-120">Header</span><span class="sxs-lookup"><span data-stu-id="a181b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a181b-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a181b-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





