---
description: Извлекает уникальный идентификатор кнопки пера.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'Метод Итаблеткурсорбуттон::'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 21d63ef0c934e96bc93b5384cab1e67f9dd452d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081245"
---
# <a name="itabletcursorbuttongetguid-method"></a><span data-ttu-id="45bdc-103">Метод Итаблеткурсорбуттон::</span><span class="sxs-lookup"><span data-stu-id="45bdc-103">ITabletCursorButton::GetGuid method</span></span>

<span data-ttu-id="45bdc-104">Извлекает уникальный идентификатор кнопки пера.</span><span class="sxs-lookup"><span data-stu-id="45bdc-104">Retrieves the unique identifier of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="45bdc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45bdc-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a><span data-ttu-id="45bdc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45bdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45bdc-107">*пгуидбтн* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="45bdc-107">*pguidBtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45bdc-108">Уникальное значение, идентифицирующее кнопку пера.</span><span class="sxs-lookup"><span data-stu-id="45bdc-108">A unique value that identifies the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45bdc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45bdc-109">Return value</span></span>

<span data-ttu-id="45bdc-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="45bdc-110">This method can return one of these values.</span></span>



| <span data-ttu-id="45bdc-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="45bdc-111">Return code</span></span>                                                                            | <span data-ttu-id="45bdc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="45bdc-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="45bdc-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="45bdc-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="45bdc-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="45bdc-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="45bdc-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="45bdc-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="45bdc-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="45bdc-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="45bdc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="45bdc-117">Requirements</span></span>



| <span data-ttu-id="45bdc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="45bdc-118">Requirement</span></span> | <span data-ttu-id="45bdc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="45bdc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45bdc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45bdc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="45bdc-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="45bdc-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="45bdc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45bdc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="45bdc-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="45bdc-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="45bdc-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45bdc-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="45bdc-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45bdc-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45bdc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45bdc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45bdc-127">**Интерфейс Итаблеткурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="45bdc-127">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




