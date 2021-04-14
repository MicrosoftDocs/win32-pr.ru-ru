---
description: Получает идентификатор пера.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'Метод Итаблеткурсор:: GetId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423986"
---
# <a name="itabletcursorgetid-method"></a><span data-ttu-id="a435f-103">Метод Итаблеткурсор:: GetId</span><span class="sxs-lookup"><span data-stu-id="a435f-103">ITabletCursor::GetId method</span></span>

<span data-ttu-id="a435f-104">Получает идентификатор пера.</span><span class="sxs-lookup"><span data-stu-id="a435f-104">Retrieves the stylus identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="a435f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a435f-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a><span data-ttu-id="a435f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a435f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a435f-107">*pCid* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a435f-107">*pCid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a435f-108">Идентификатор пера планшета.</span><span class="sxs-lookup"><span data-stu-id="a435f-108">The identifier of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a435f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a435f-109">Return value</span></span>

<span data-ttu-id="a435f-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a435f-110">This method can return one of these values.</span></span>



| <span data-ttu-id="a435f-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a435f-111">Return code</span></span>                                                                            | <span data-ttu-id="a435f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a435f-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a435f-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a435f-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a435f-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a435f-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="a435f-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a435f-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a435f-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a435f-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a435f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a435f-117">Remarks</span></span>

<span data-ttu-id="a435f-118">Идентификатор КУРСОРа \_ определен как DWORD.</span><span class="sxs-lookup"><span data-stu-id="a435f-118">CURSOR\_ID is defined as a DWORD.</span></span>

## <a name="requirements"></a><span data-ttu-id="a435f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a435f-119">Requirements</span></span>



| <span data-ttu-id="a435f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a435f-120">Requirement</span></span> | <span data-ttu-id="a435f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a435f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a435f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a435f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a435f-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a435f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a435f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a435f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a435f-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a435f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a435f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a435f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a435f-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a435f-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a435f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a435f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a435f-129">**Интерфейс Итаблеткурсор**</span><span class="sxs-lookup"><span data-stu-id="a435f-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




