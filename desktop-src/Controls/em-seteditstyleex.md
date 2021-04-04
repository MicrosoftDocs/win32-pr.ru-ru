---
title: Сообщение EM_SETEDITSTYLEEX (RichEdit. h)
description: Задает текущие расширенные флаги стиля правки.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- Элементы управления Windows для EM_SETEDITSTYLEEX сообщений
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989190"
---
# <a name="em_seteditstyleex-message"></a><span data-ttu-id="f940b-104">\_Сообщение СЕТЕДИТСТИЛИКС EM</span><span class="sxs-lookup"><span data-stu-id="f940b-104">EM\_SETEDITSTYLEEX message</span></span>

<span data-ttu-id="f940b-105">Задает текущие расширенные флаги стиля правки.</span><span class="sxs-lookup"><span data-stu-id="f940b-105">Sets the current extended edit style flags.</span></span>


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a><span data-ttu-id="f940b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f940b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f940b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f940b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f940b-108">Указывает один или несколько расширенных флагов стиля редактирования.</span><span class="sxs-lookup"><span data-stu-id="f940b-108">Specifies one or more extended edit style flags.</span></span> <span data-ttu-id="f940b-109">Список возможных значений см. в разделе [**EM \_ жетедитстиликс**](/windows/desktop/Controls/em-geteditstyleex).</span><span class="sxs-lookup"><span data-stu-id="f940b-109">For a list of possible values, see [**EM\_GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span></span>

</dd> <dt>

<span data-ttu-id="f940b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f940b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f940b-111">Маска, состоящая из одного или нескольких значений *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f940b-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="f940b-112">Будут установлены или сняты только значения, указанные в этой маске.</span><span class="sxs-lookup"><span data-stu-id="f940b-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="f940b-113">Это позволяет устанавливать или снимать один флаг без считывания текущих состояний флагов.</span><span class="sxs-lookup"><span data-stu-id="f940b-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f940b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f940b-114">Return value</span></span>

<span data-ttu-id="f940b-115">Возвращаемое значение является состоянием расширенных флагов стиля правки после того, как Расширенное редактирование попытается применить изменения стиля редактирования.</span><span class="sxs-lookup"><span data-stu-id="f940b-115">The return value is the state of the extended edit style flags after rich edit has attempted to implement your edit style changes.</span></span> <span data-ttu-id="f940b-116">Флаги редактирования стиля представляют собой набор флагов, указывающих текущий стиль редактирования.</span><span class="sxs-lookup"><span data-stu-id="f940b-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f940b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f940b-117">Requirements</span></span>



| <span data-ttu-id="f940b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f940b-118">Requirement</span></span> | <span data-ttu-id="f940b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f940b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f940b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f940b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f940b-121">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f940b-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f940b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f940b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f940b-123">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f940b-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f940b-124">Header</span><span class="sxs-lookup"><span data-stu-id="f940b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f940b-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f940b-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f940b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f940b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f940b-127">**EM \_ жетедитстиликс**</span><span class="sxs-lookup"><span data-stu-id="f940b-127">**EM\_GETEDITSTYLEEX**</span></span>](em-geteditstyleex.md)
</dt> </dl>

 

