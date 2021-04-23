---
title: Тсвиевкукие (Текстстор. h)
description: Тип данных Тсвиевкукие определяет представление контекста.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- тсвиевкукие
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681819"
---
# <a name="tsviewcookie"></a><span data-ttu-id="37a53-104">тсвиевкукие</span><span class="sxs-lookup"><span data-stu-id="37a53-104">TsViewCookie</span></span>

<span data-ttu-id="37a53-105">Тип данных **тсвиевкукие** определяет представление контекста.</span><span class="sxs-lookup"><span data-stu-id="37a53-105">The **TsViewCookie** data type identifies a context view.</span></span>


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a><span data-ttu-id="37a53-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37a53-106">Remarks</span></span>

<span data-ttu-id="37a53-107">Приложение должно предоставить уникальное значение **тсвиевкукие** для каждого создаваемого представления.</span><span class="sxs-lookup"><span data-stu-id="37a53-107">An application must supply a unique **TsViewCookie** value for each view it creates.</span></span>

<span data-ttu-id="37a53-108">Диспетчер TSF получает это значение из приложения путем вызова [ITextStoreACP:: жетактивевиев](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) или [Итекстстореанчор:: жетактивевиев](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span><span class="sxs-lookup"><span data-stu-id="37a53-108">The TSF manager obtains this value from the application by calling [ITextStoreACP::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) or [ITextStoreAnchor::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span></span> <span data-ttu-id="37a53-109">Диспетчер TSF использует это значение для обнаружения представления при вызове различных методов [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) или [итекстстореанчор](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="37a53-109">The TSF manager uses this value to identify the view when calling various [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) or [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="37a53-110">Требования</span><span class="sxs-lookup"><span data-stu-id="37a53-110">Requirements</span></span>



| <span data-ttu-id="37a53-111">Требование</span><span class="sxs-lookup"><span data-stu-id="37a53-111">Requirement</span></span> | <span data-ttu-id="37a53-112">Значение</span><span class="sxs-lookup"><span data-stu-id="37a53-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37a53-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37a53-113">Minimum supported client</span></span><br/> | <span data-ttu-id="37a53-114">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="37a53-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="37a53-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37a53-115">Minimum supported server</span></span><br/> | <span data-ttu-id="37a53-116">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="37a53-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="37a53-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="37a53-117">Redistributable</span></span><br/>          | <span data-ttu-id="37a53-118">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="37a53-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="37a53-119">Header</span><span class="sxs-lookup"><span data-stu-id="37a53-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="37a53-120"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="37a53-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="37a53-121">IDL</span><span class="sxs-lookup"><span data-stu-id="37a53-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37a53-122"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="37a53-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37a53-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37a53-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a53-124">**ITextStoreACP**</span><span class="sxs-lookup"><span data-stu-id="37a53-124">**ITextStoreACP**</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="37a53-125">**ITextStoreACP:: Жетактивевиев**</span><span class="sxs-lookup"><span data-stu-id="37a53-125">**ITextStoreACP::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[<span data-ttu-id="37a53-126">**Итекстстореанчор:: Жетактивевиев**</span><span class="sxs-lookup"><span data-stu-id="37a53-126">**ITextStoreAnchor::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





