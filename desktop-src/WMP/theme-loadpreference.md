---
title: THEME. Лоадпреференце
description: Метод Лоадпреференце загружает предпочтение из реестра.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- Проигрыватель Windows Media THEME. Лоадпреференце
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680090"
---
# <a name="themeloadpreference"></a><span data-ttu-id="280a0-104">THEME. Лоадпреференце</span><span class="sxs-lookup"><span data-stu-id="280a0-104">THEME.loadPreference</span></span>

<span data-ttu-id="280a0-105">Метод **лоадпреференце** загружает предпочтение из реестра.</span><span class="sxs-lookup"><span data-stu-id="280a0-105">The **loadPreference** method loads a preference from the registry.</span></span>

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a><span data-ttu-id="280a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="280a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="280a0-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*секэй*</span><span class="sxs-lookup"><span data-stu-id="280a0-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="280a0-108">**Строка** , указывающая ключ значения предпочтения для загрузки.</span><span class="sxs-lookup"><span data-stu-id="280a0-108">A **String** specifying the key of the preference value to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="280a0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="280a0-109">Return Value</span></span>

<span data-ttu-id="280a0-110">Этот метод возвращает **строку**.</span><span class="sxs-lookup"><span data-stu-id="280a0-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="280a0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="280a0-111">Remarks</span></span>

<span data-ttu-id="280a0-112">Предпочтение — это пара "ключ-значение", которая может храниться в реестре для сохранения сведений о состоянии проигрывателя Windows Media между запусками.</span><span class="sxs-lookup"><span data-stu-id="280a0-112">A preference is a key/value pair that can be stored in the registry to retain information about the state of the Windows Media Player between runs.</span></span> <span data-ttu-id="280a0-113">Эта функция может использоваться, например, для сохранения параметров настройки, чтобы их не нужно было повторно указывать каждый раз при запуске проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="280a0-113">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="280a0-114">Параметры не шифруются и поэтому не являются безопасным методом для сохранения данных.</span><span class="sxs-lookup"><span data-stu-id="280a0-114">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="280a0-115">Не используйте настройки для хранения частных данных.</span><span class="sxs-lookup"><span data-stu-id="280a0-115">Do not use preferences to store private data.</span></span>

## <a name="requirements"></a><span data-ttu-id="280a0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="280a0-116">Requirements</span></span>



| <span data-ttu-id="280a0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="280a0-117">Requirement</span></span> | <span data-ttu-id="280a0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="280a0-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="280a0-119">Версия</span><span class="sxs-lookup"><span data-stu-id="280a0-119">Version</span></span><br/> | <span data-ttu-id="280a0-120">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="280a0-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="280a0-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="280a0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="280a0-122">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="280a0-122">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="280a0-123">**THEME. Савепреференце**</span><span class="sxs-lookup"><span data-stu-id="280a0-123">**THEME.savePreference**</span></span>](theme-savepreference.md)
</dt> </dl>

 

 





