---
description: Изменяет текст заголовка указанного окна (если он имеется).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: Функция _SetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649041"
---
# <a name="_setwindowtext-function"></a><span data-ttu-id="ca035-103">\_Функция SetWindowText</span><span class="sxs-lookup"><span data-stu-id="ca035-103">\_SetWindowText function</span></span>

<span data-ttu-id="ca035-104">\[Эта функция является оболочкой для функции **SetWindowText** .</span><span class="sxs-lookup"><span data-stu-id="ca035-104">\[This function is a wrapper over the **SetWindowText** function.</span></span> <span data-ttu-id="ca035-105">Эта функция может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="ca035-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="ca035-106">Приложения должны вызывать **SetWindowText** напрямую.\]</span><span class="sxs-lookup"><span data-stu-id="ca035-106">Applications should call **SetWindowText** directly.\]</span></span>

<span data-ttu-id="ca035-107">Изменяет текст заголовка указанного окна (если он имеется).</span><span class="sxs-lookup"><span data-stu-id="ca035-107">Changes the text of the specified window's title bar (if it has one).</span></span> <span data-ttu-id="ca035-108">См. [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="ca035-108">See [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca035-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca035-109">Syntax</span></span>


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="ca035-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca035-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca035-111">*...*</span><span class="sxs-lookup"><span data-stu-id="ca035-111">*...*</span></span> 
<span data-ttu-id="ca035-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ca035-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ca035-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ca035-113">Requirements</span></span>



| <span data-ttu-id="ca035-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ca035-114">Requirement</span></span> | <span data-ttu-id="ca035-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ca035-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca035-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ca035-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ca035-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca035-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca035-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca035-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca035-119">**SetWindowText**</span><span class="sxs-lookup"><span data-stu-id="ca035-119">**SetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
