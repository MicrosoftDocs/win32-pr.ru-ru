---
description: Обновляет планшет дигитайзер до координат сопоставления расположения окна.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'Метод Итаблетконтекстп:: Траккинпутрект'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712811"
---
# <a name="itabletcontextptrackinputrect-method"></a><span data-ttu-id="e6325-103">Метод Итаблетконтекстп:: Траккинпутрект</span><span class="sxs-lookup"><span data-stu-id="e6325-103">ITabletContextP::TrackInputRect method</span></span>

<span data-ttu-id="e6325-104">Обновляет планшет дигитайзер до координат сопоставления расположения окна.</span><span class="sxs-lookup"><span data-stu-id="e6325-104">Updates the tablet digitizer to window location mapping coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6325-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6325-105">Syntax</span></span>


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="e6325-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6325-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6325-107">*прЦинпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e6325-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6325-108">Новый прямоугольник входного окна после обновления сопоставления между координатами окна и дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="e6325-108">The new input window rectangle after updating the mapping between the window and digitizer coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6325-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6325-109">Return value</span></span>

<span data-ttu-id="e6325-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e6325-110">This method can return one of these values.</span></span>



| <span data-ttu-id="e6325-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e6325-111">Return code</span></span>                                                                            | <span data-ttu-id="e6325-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e6325-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e6325-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e6325-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e6325-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e6325-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e6325-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="e6325-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e6325-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e6325-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6325-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6325-117">Remarks</span></span>

<span data-ttu-id="e6325-118">Вызывайте этот метод всякий раз, когда изменяется положение окна на экране.</span><span class="sxs-lookup"><span data-stu-id="e6325-118">Call this method anytime the location of the window on the screen changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6325-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e6325-119">Requirements</span></span>



| <span data-ttu-id="e6325-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e6325-120">Requirement</span></span> | <span data-ttu-id="e6325-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e6325-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6325-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6325-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e6325-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e6325-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e6325-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6325-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e6325-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6325-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e6325-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6325-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6325-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6325-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6325-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6325-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6325-129">**Интерфейс Итаблетконтекстп**</span><span class="sxs-lookup"><span data-stu-id="e6325-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




