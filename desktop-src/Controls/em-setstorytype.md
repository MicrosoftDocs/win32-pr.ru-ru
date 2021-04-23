---
title: Сообщение EM_SETSTORYTYPE (RichEdit. h)
description: Задает тип истории.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- Элементы управления Windows для EM_SETSTORYTYPE сообщений
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891714"
---
# <a name="em_setstorytype-message"></a><span data-ttu-id="ec621-104">\_Сообщение СЕТСТОРИТИПЕ EM</span><span class="sxs-lookup"><span data-stu-id="ec621-104">EM\_SETSTORYTYPE message</span></span>

<span data-ttu-id="ec621-105">Задает тип истории.</span><span class="sxs-lookup"><span data-stu-id="ec621-105">Sets the story type.</span></span>


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a><span data-ttu-id="ec621-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec621-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec621-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec621-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec621-108">Индекс истории.</span><span class="sxs-lookup"><span data-stu-id="ec621-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="ec621-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec621-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec621-110">Новый тип истории.</span><span class="sxs-lookup"><span data-stu-id="ec621-110">The new story type.</span></span> <span data-ttu-id="ec621-111">Список типов истории см. в разделе [**EM \_ жетсторитипе**](em-getstorytype.md).</span><span class="sxs-lookup"><span data-stu-id="ec621-111">For a list of story types, see [**EM\_GETSTORYTYPE**](em-getstorytype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec621-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec621-112">Return value</span></span>

<span data-ttu-id="ec621-113">Заданный тип истории.</span><span class="sxs-lookup"><span data-stu-id="ec621-113">The story type that was set.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec621-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ec621-114">Requirements</span></span>



| <span data-ttu-id="ec621-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ec621-115">Requirement</span></span> | <span data-ttu-id="ec621-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ec621-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec621-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec621-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ec621-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ec621-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ec621-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec621-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ec621-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ec621-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec621-121">Header</span><span class="sxs-lookup"><span data-stu-id="ec621-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec621-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec621-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





