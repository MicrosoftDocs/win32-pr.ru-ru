---
description: Указывает, является ли перо перевернутым.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'Метод Итаблеткурсор:: инверсия'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656641"
---
# <a name="itabletcursorisinverted-method"></a><span data-ttu-id="d22e9-103">Метод Итаблеткурсор:: инверсия</span><span class="sxs-lookup"><span data-stu-id="d22e9-103">ITabletCursor::IsInverted method</span></span>

<span data-ttu-id="d22e9-104">Указывает, является ли перо перевернутым.</span><span class="sxs-lookup"><span data-stu-id="d22e9-104">Indicates if the stylus is upside down.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d22e9-105">Syntax</span></span>


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a><span data-ttu-id="d22e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d22e9-106">Parameters</span></span>

<span data-ttu-id="d22e9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d22e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d22e9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d22e9-108">Return value</span></span>

<span data-ttu-id="d22e9-109">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d22e9-109">This method can return one of these values.</span></span>



| <span data-ttu-id="d22e9-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d22e9-110">Return code</span></span>                                                                             | <span data-ttu-id="d22e9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d22e9-111">Description</span></span>                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d22e9-112"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d22e9-112"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d22e9-113">Перо инвертировано.</span><span class="sxs-lookup"><span data-stu-id="d22e9-113">The stylus is inverted.</span></span><br/>        |
| <dl> <span data-ttu-id="d22e9-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d22e9-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d22e9-115">Перо не инвертировано.</span><span class="sxs-lookup"><span data-stu-id="d22e9-115">The stylus is not inverted.</span></span><br/>    |
| <dl> <span data-ttu-id="d22e9-116"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="d22e9-116"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="d22e9-117">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d22e9-117">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d22e9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d22e9-118">Requirements</span></span>



| <span data-ttu-id="d22e9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d22e9-119">Requirement</span></span> | <span data-ttu-id="d22e9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d22e9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d22e9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d22e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d22e9-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d22e9-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d22e9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d22e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d22e9-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d22e9-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d22e9-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d22e9-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d22e9-126"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d22e9-126"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d22e9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d22e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22e9-128">**итаблеткурсор**</span><span class="sxs-lookup"><span data-stu-id="d22e9-128">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="d22e9-129">**Интерфейс Итаблеткурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="d22e9-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




