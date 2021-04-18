---
title: THEME. Савепреференце
description: Метод Савепреференце сохраняет предпочтение в реестре.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- Проигрыватель Windows Media THEME. Савепреференце
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708436"
---
# <a name="themesavepreference"></a><span data-ttu-id="314c8-104">THEME. Савепреференце</span><span class="sxs-lookup"><span data-stu-id="314c8-104">THEME.savePreference</span></span>

<span data-ttu-id="314c8-105">Метод **савепреференце** сохраняет предпочтение в реестре.</span><span class="sxs-lookup"><span data-stu-id="314c8-105">The **savePreference** method saves a preference in the registry.</span></span>

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a><span data-ttu-id="314c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="314c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314c8-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*секэй*</span><span class="sxs-lookup"><span data-stu-id="314c8-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="314c8-108">**Строка** , указывающая ключ значения предпочтения для сохранения.</span><span class="sxs-lookup"><span data-stu-id="314c8-108">A **String** specifying the key of the preference value to save.</span></span>

</dd> <dt>

<span data-ttu-id="314c8-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*Значение типа представляющее*</span><span class="sxs-lookup"><span data-stu-id="314c8-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*</span></span>
</dt> <dd>

<span data-ttu-id="314c8-110">**Строка** , указывающая значение для сохранения.</span><span class="sxs-lookup"><span data-stu-id="314c8-110">A **String** specifying the value to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314c8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="314c8-111">Return Value</span></span>

<span data-ttu-id="314c8-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="314c8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="314c8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="314c8-113">Remarks</span></span>

<span data-ttu-id="314c8-114">Предпочтение — это пара "ключ-значение", которая может храниться в реестре для сохранения сведений о состоянии проигрывателя Windows Media между запусками.</span><span class="sxs-lookup"><span data-stu-id="314c8-114">A preference is a key/value pair that can be stored in the registry to retain information about the state of Windows Media Player between runs.</span></span> <span data-ttu-id="314c8-115">Эта функция может использоваться, например, для сохранения параметров настройки, чтобы их не нужно было повторно указывать каждый раз при запуске проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="314c8-115">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="314c8-116">Параметры не шифруются и поэтому не являются безопасным методом для сохранения данных.</span><span class="sxs-lookup"><span data-stu-id="314c8-116">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="314c8-117">Не используйте настройки для хранения частных данных.</span><span class="sxs-lookup"><span data-stu-id="314c8-117">Do not use preferences to store private data.</span></span>

## <a name="examples"></a><span data-ttu-id="314c8-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="314c8-118">Examples</span></span>


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="314c8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="314c8-119">Requirements</span></span>



| <span data-ttu-id="314c8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="314c8-120">Requirement</span></span> | <span data-ttu-id="314c8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="314c8-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="314c8-122">Версия</span><span class="sxs-lookup"><span data-stu-id="314c8-122">Version</span></span><br/> | <span data-ttu-id="314c8-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="314c8-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="314c8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="314c8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314c8-125">**Элемент THEME**</span><span class="sxs-lookup"><span data-stu-id="314c8-125">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="314c8-126">**THEME. Лоадпреференце**</span><span class="sxs-lookup"><span data-stu-id="314c8-126">**THEME.loadPreference**</span></span>](theme-loadpreference.md)
</dt> </dl>

 

 





