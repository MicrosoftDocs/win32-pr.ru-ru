---
description: Получает количество кнопок пера планшета.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: 'Метод Итаблеткурсор:: Жетбуттонкаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719696"
---
# <a name="itabletcursorgetbuttoncount-method"></a><span data-ttu-id="53d22-103">Метод Итаблеткурсор:: Жетбуттонкаунт</span><span class="sxs-lookup"><span data-stu-id="53d22-103">ITabletCursor::GetButtonCount method</span></span>

<span data-ttu-id="53d22-104">Получает количество кнопок пера планшета.</span><span class="sxs-lookup"><span data-stu-id="53d22-104">Retrieves the number of buttons on the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d22-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53d22-105">Syntax</span></span>


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a><span data-ttu-id="53d22-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53d22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d22-107">*пкбуттонс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="53d22-107">*pcButtons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53d22-108">Число кнопок пера планшета.</span><span class="sxs-lookup"><span data-stu-id="53d22-108">The count of buttons on the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53d22-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53d22-109">Return value</span></span>

<span data-ttu-id="53d22-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="53d22-110">This method can return one of these values.</span></span>



| <span data-ttu-id="53d22-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="53d22-111">Return code</span></span>                                                                            | <span data-ttu-id="53d22-112">Описание</span><span class="sxs-lookup"><span data-stu-id="53d22-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="53d22-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="53d22-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="53d22-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="53d22-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="53d22-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="53d22-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="53d22-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="53d22-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="53d22-117">Требования</span><span class="sxs-lookup"><span data-stu-id="53d22-117">Requirements</span></span>



| <span data-ttu-id="53d22-118">Требование</span><span class="sxs-lookup"><span data-stu-id="53d22-118">Requirement</span></span> | <span data-ttu-id="53d22-119">Значение</span><span class="sxs-lookup"><span data-stu-id="53d22-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53d22-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53d22-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53d22-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="53d22-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="53d22-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53d22-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53d22-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="53d22-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="53d22-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53d22-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="53d22-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53d22-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53d22-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53d22-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d22-127">**Интерфейс Итаблеткурсор**</span><span class="sxs-lookup"><span data-stu-id="53d22-127">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




