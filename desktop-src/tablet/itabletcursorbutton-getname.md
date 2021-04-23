---
description: Возвращает имя кнопки пера.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: 'Метод Итаблеткурсорбуттон:: Name'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683638"
---
# <a name="itabletcursorbuttongetname-method"></a><span data-ttu-id="b280e-103">Метод Итаблеткурсорбуттон:: Name</span><span class="sxs-lookup"><span data-stu-id="b280e-103">ITabletCursorButton::GetName method</span></span>

<span data-ttu-id="b280e-104">Возвращает имя кнопки пера.</span><span class="sxs-lookup"><span data-stu-id="b280e-104">Retrieves the name of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="b280e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b280e-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="b280e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b280e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b280e-107">*ппвсзнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b280e-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b280e-108">Имя кнопки пера.</span><span class="sxs-lookup"><span data-stu-id="b280e-108">The name of the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b280e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b280e-109">Return value</span></span>

<span data-ttu-id="b280e-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b280e-110">This method can return one of these values.</span></span>



| <span data-ttu-id="b280e-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b280e-111">Return code</span></span>                                                                            | <span data-ttu-id="b280e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b280e-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="b280e-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b280e-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b280e-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b280e-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="b280e-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="b280e-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b280e-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b280e-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b280e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b280e-117">Remarks</span></span>

<span data-ttu-id="b280e-118">Он отвечает за освобождение памяти, возвращаемой этим методом, с помощью [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="b280e-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="b280e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b280e-119">Requirements</span></span>



| <span data-ttu-id="b280e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b280e-120">Requirement</span></span> | <span data-ttu-id="b280e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b280e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b280e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b280e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b280e-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b280e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b280e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b280e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b280e-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b280e-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b280e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b280e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b280e-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b280e-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b280e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b280e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b280e-129">**Интерфейс Итаблеткурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="b280e-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

