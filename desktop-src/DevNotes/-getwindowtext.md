---
description: Извлекает текст из заголовков указанного окна.
ms.assetid: c14151f9-222f-40a2-837e-7f9a728efc82
title: Функция _GetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 61c84c8a5f00ad97b8a76ef4139b20b74f1be085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648029"
---
# <a name="_getwindowtext-function"></a><span data-ttu-id="d54eb-103">\_Функция Жетвиндовтекст</span><span class="sxs-lookup"><span data-stu-id="d54eb-103">\_GetWindowText function</span></span>

<span data-ttu-id="d54eb-104">\[Эта функция является оболочкой для функции **жетвиндовтекст** .</span><span class="sxs-lookup"><span data-stu-id="d54eb-104">\[This function is a wrapper over the **GetWindowText** function.</span></span> <span data-ttu-id="d54eb-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="d54eb-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="d54eb-106">Приложения должны вызывать **жетвиндовтекст** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="d54eb-106">Applications should call **GetWindowText** directly.\]</span></span>

<span data-ttu-id="d54eb-107">Извлекает текст из заголовков указанного окна.</span><span class="sxs-lookup"><span data-stu-id="d54eb-107">Retrieves the text from the specified window's title bar.</span></span> <span data-ttu-id="d54eb-108">См. [**жетвиндовтекст**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="d54eb-108">See [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="d54eb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d54eb-109">Syntax</span></span>


```C++
int _GetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="d54eb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d54eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d54eb-111">*...*</span><span class="sxs-lookup"><span data-stu-id="d54eb-111">*...*</span></span> 
<span data-ttu-id="d54eb-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d54eb-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d54eb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d54eb-113">Requirements</span></span>



| <span data-ttu-id="d54eb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d54eb-114">Requirement</span></span> | <span data-ttu-id="d54eb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d54eb-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d54eb-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d54eb-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d54eb-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d54eb-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d54eb-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d54eb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54eb-119">**жетвиндовтекст**</span><span class="sxs-lookup"><span data-stu-id="d54eb-119">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> </dl>

 

 
