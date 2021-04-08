---
description: Извлекает прямоугольник, представляющий максимальную область ввода планшета.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'Метод Итаблет:: Жетмаксинпутрект'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: de2649fe7410e6d335f653c09bfe86a8ddaac813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911716"
---
# <a name="itabletgetmaxinputrect-method"></a><span data-ttu-id="81dce-103">Метод Итаблет:: Жетмаксинпутрект</span><span class="sxs-lookup"><span data-stu-id="81dce-103">ITablet::GetMaxInputRect method</span></span>

<span data-ttu-id="81dce-104">Извлекает прямоугольник, представляющий максимальную область ввода планшета.</span><span class="sxs-lookup"><span data-stu-id="81dce-104">Retrieves a rectangle that represents maximum input area of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="81dce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81dce-105">Syntax</span></span>


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="81dce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81dce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81dce-107">*прЦинпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81dce-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81dce-108">Указатель на прямоугольник, представляющий максимальную область ввода планшета.</span><span class="sxs-lookup"><span data-stu-id="81dce-108">Pointer to rectangle that represents maximum input area of the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81dce-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81dce-109">Return value</span></span>

<span data-ttu-id="81dce-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="81dce-110">This method can return one of these values.</span></span>



| <span data-ttu-id="81dce-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="81dce-111">Return code</span></span>                                                                            | <span data-ttu-id="81dce-112">Описание</span><span class="sxs-lookup"><span data-stu-id="81dce-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="81dce-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="81dce-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="81dce-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="81dce-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="81dce-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="81dce-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="81dce-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="81dce-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81dce-117">Требования</span><span class="sxs-lookup"><span data-stu-id="81dce-117">Requirements</span></span>



| <span data-ttu-id="81dce-118">Требование</span><span class="sxs-lookup"><span data-stu-id="81dce-118">Requirement</span></span> | <span data-ttu-id="81dce-119">Значение</span><span class="sxs-lookup"><span data-stu-id="81dce-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81dce-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81dce-120">Minimum supported client</span></span><br/> | <span data-ttu-id="81dce-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="81dce-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="81dce-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81dce-122">Minimum supported server</span></span><br/> | <span data-ttu-id="81dce-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="81dce-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="81dce-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81dce-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="81dce-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81dce-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81dce-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81dce-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81dce-127">**Интерфейс Итаблет**</span><span class="sxs-lookup"><span data-stu-id="81dce-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




