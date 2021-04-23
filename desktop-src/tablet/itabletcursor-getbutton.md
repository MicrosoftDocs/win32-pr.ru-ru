---
description: Извлекает указанный объект кнопки из пера планшета.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'Метод Итаблеткурсор:: "Button"'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712359"
---
# <a name="itabletcursorgetbutton-method"></a><span data-ttu-id="6f6db-103">Метод Итаблеткурсор:: "Button"</span><span class="sxs-lookup"><span data-stu-id="6f6db-103">ITabletCursor::GetButton method</span></span>

<span data-ttu-id="6f6db-104">Извлекает указанный объект кнопки из пера планшета.</span><span class="sxs-lookup"><span data-stu-id="6f6db-104">Retrieves the specified button object from a tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f6db-105">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a><span data-ttu-id="6f6db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f6db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f6db-107">*ибуттон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f6db-107">*iButton* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f6db-108">Идентификатор извлекаемой кнопки.</span><span class="sxs-lookup"><span data-stu-id="6f6db-108">Identifier of the button to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6f6db-109">*ппбуттон* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6f6db-109">*ppButton* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f6db-110">Объект Button, заданный параметром *ибуттон* .</span><span class="sxs-lookup"><span data-stu-id="6f6db-110">The button object specified by the *iButton* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f6db-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f6db-111">Return value</span></span>

<span data-ttu-id="6f6db-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="6f6db-112">This method can return one of these values.</span></span>



| <span data-ttu-id="6f6db-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6f6db-113">Return code</span></span>                                                                            | <span data-ttu-id="6f6db-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6f6db-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="6f6db-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6f6db-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="6f6db-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="6f6db-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="6f6db-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="6f6db-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="6f6db-118">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6f6db-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6f6db-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6f6db-119">Requirements</span></span>



| <span data-ttu-id="6f6db-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6f6db-120">Requirement</span></span> | <span data-ttu-id="6f6db-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6f6db-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6db-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f6db-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6f6db-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6f6db-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6f6db-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f6db-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6f6db-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6f6db-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6f6db-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f6db-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f6db-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f6db-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f6db-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f6db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f6db-129">**Интерфейс Итаблеткурсор**</span><span class="sxs-lookup"><span data-stu-id="6f6db-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




