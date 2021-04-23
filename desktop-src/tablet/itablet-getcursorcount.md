---
description: Возвращает число объектов Cursor, связанных с планшетом.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'Метод Итаблет:: Жеткурсоркаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719657"
---
# <a name="itabletgetcursorcount-method"></a><span data-ttu-id="c68b3-103">Метод Итаблет:: Жеткурсоркаунт</span><span class="sxs-lookup"><span data-stu-id="c68b3-103">ITablet::GetCursorCount method</span></span>

<span data-ttu-id="c68b3-104">Возвращает число объектов Cursor, связанных с планшетом.</span><span class="sxs-lookup"><span data-stu-id="c68b3-104">Returns the number of cursor objects associated with the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c68b3-105">Syntax</span></span>


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a><span data-ttu-id="c68b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c68b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68b3-107">*пккурс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c68b3-107">*pcCurs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c68b3-108">Число объектов Cursor, связанных с планшетом.</span><span class="sxs-lookup"><span data-stu-id="c68b3-108">The number of cursor objects associated with the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c68b3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c68b3-109">Return value</span></span>

<span data-ttu-id="c68b3-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c68b3-110">This method can return one of these values.</span></span>



| <span data-ttu-id="c68b3-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c68b3-111">Return code</span></span>                                                                            | <span data-ttu-id="c68b3-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c68b3-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c68b3-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c68b3-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c68b3-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c68b3-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="c68b3-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="c68b3-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c68b3-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c68b3-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c68b3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c68b3-117">Requirements</span></span>



| <span data-ttu-id="c68b3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c68b3-118">Requirement</span></span> | <span data-ttu-id="c68b3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c68b3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c68b3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c68b3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c68b3-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c68b3-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c68b3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c68b3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c68b3-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c68b3-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c68b3-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c68b3-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="c68b3-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c68b3-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68b3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c68b3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68b3-127">**Интерфейс Итаблет**</span><span class="sxs-lookup"><span data-stu-id="c68b3-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




