---
title: Метод DVD. Back
description: Метод Back Возвращает отображение из подменю в родительское меню.
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- метод обратной передачи Windows Media Player
- метод обратной передачи Windows Media Player, класс DVD
- Класс DVD проигрыватель Windows Media Player, метод Back
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e656051d02ec5efc74aa7595d2ca6cb20e648f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415541"
---
# <a name="dvdback-method"></a><span data-ttu-id="a4cda-106">Метод DVD. Back</span><span class="sxs-lookup"><span data-stu-id="a4cda-106">DVD.back method</span></span>

<span data-ttu-id="a4cda-107">Метод **Back** Возвращает отображение из подменю в родительское меню.</span><span class="sxs-lookup"><span data-stu-id="a4cda-107">The **back** method returns the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4cda-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4cda-108">Syntax</span></span>


```JScript
DVD.back()
```



## <a name="parameters"></a><span data-ttu-id="a4cda-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4cda-109">Parameters</span></span>

<span data-ttu-id="a4cda-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a4cda-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4cda-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4cda-111">Return value</span></span>

<span data-ttu-id="a4cda-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a4cda-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4cda-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4cda-113">Remarks</span></span>

<span data-ttu-id="a4cda-114">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="a4cda-114">Every DVD is authored differently.</span></span> <span data-ttu-id="a4cda-115">Некоторые DVD-диски созданы таким образом, что метод **Back** доступен из корневого меню, но при вызове он не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="a4cda-115">Some DVDs are authored so that the **back** method is available from the root menu, but when invoked, it will do nothing.</span></span>

<span data-ttu-id="a4cda-116">**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда выполняется, но не выполняет требуемую операцию.</span><span class="sxs-lookup"><span data-stu-id="a4cda-116">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4cda-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a4cda-117">Requirements</span></span>



| <span data-ttu-id="a4cda-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a4cda-118">Requirement</span></span> | <span data-ttu-id="a4cda-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a4cda-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4cda-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4cda-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a4cda-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a4cda-121">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4cda-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4cda-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a4cda-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4cda-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a4cda-124">Версия</span><span class="sxs-lookup"><span data-stu-id="a4cda-124">Version</span></span><br/>                  | <span data-ttu-id="a4cda-125">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a4cda-125">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="a4cda-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a4cda-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4cda-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4cda-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4cda-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4cda-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4cda-129">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="a4cda-129">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





