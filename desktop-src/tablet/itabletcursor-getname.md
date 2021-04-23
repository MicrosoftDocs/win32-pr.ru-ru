---
description: Извлекает имя пера планшета.
ms.assetid: 94955c04-f699-428b-b4bf-53919b61b1ab
title: 'Метод Итаблеткурсор:: Name'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b9d984d5eb711c2344ba0f9fb2dbf410a7d49bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999426"
---
# <a name="itabletcursorgetname-method"></a><span data-ttu-id="aa6fa-103">Метод Итаблеткурсор:: Name</span><span class="sxs-lookup"><span data-stu-id="aa6fa-103">ITabletCursor::GetName method</span></span>

<span data-ttu-id="aa6fa-104">Извлекает имя пера планшета.</span><span class="sxs-lookup"><span data-stu-id="aa6fa-104">Retrieves the name of the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa6fa-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="aa6fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa6fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa6fa-107">*ппвсзнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aa6fa-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6fa-108">Имя пера планшета.</span><span class="sxs-lookup"><span data-stu-id="aa6fa-108">The name of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa6fa-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa6fa-109">Return value</span></span>

<span data-ttu-id="aa6fa-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="aa6fa-110">This method can return one of these values.</span></span>



| <span data-ttu-id="aa6fa-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="aa6fa-111">Return code</span></span>                                                                            | <span data-ttu-id="aa6fa-112">Описание</span><span class="sxs-lookup"><span data-stu-id="aa6fa-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="aa6fa-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="aa6fa-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="aa6fa-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="aa6fa-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="aa6fa-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="aa6fa-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="aa6fa-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="aa6fa-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa6fa-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa6fa-117">Remarks</span></span>

<span data-ttu-id="aa6fa-118">Он отвечает за освобождение памяти, возвращаемой этим методом, с помощью [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="aa6fa-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa6fa-119">Требования</span><span class="sxs-lookup"><span data-stu-id="aa6fa-119">Requirements</span></span>



| <span data-ttu-id="aa6fa-120">Требование</span><span class="sxs-lookup"><span data-stu-id="aa6fa-120">Requirement</span></span> | <span data-ttu-id="aa6fa-121">Значение</span><span class="sxs-lookup"><span data-stu-id="aa6fa-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6fa-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa6fa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aa6fa-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="aa6fa-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aa6fa-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa6fa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aa6fa-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aa6fa-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="aa6fa-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aa6fa-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa6fa-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa6fa-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa6fa-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa6fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6fa-129">**итаблеткурсор**</span><span class="sxs-lookup"><span data-stu-id="aa6fa-129">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="aa6fa-130">**Интерфейс Итаблеткурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="aa6fa-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

