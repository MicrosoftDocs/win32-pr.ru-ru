---
title: ИВМПДВД, свойство домена
description: Свойство Domain получает текущий домен DVD-диска.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Проигрыватель Windows Media, свойство домена
- свойство домена проигрыватель Windows Media Player, интерфейс ИВМПДВД
- Интерфейс ИВМПДВД Windows Media Player, свойство Domain
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652183"
---
# <a name="iwmpdvddomain-property"></a><span data-ttu-id="a34e6-106">ИВМПДВД: свойство омаин:d</span><span class="sxs-lookup"><span data-stu-id="a34e6-106">IWMPDVD::domain property</span></span>

<span data-ttu-id="a34e6-107">Свойство **domain** получает текущий домен DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="a34e6-107">The **domain** property gets the current domain of the DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="a34e6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a34e6-108">Syntax</span></span>


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a><span data-ttu-id="a34e6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a34e6-109">Property value</span></span>

<span data-ttu-id="a34e6-110">**Строка System. String** , которая является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a34e6-110">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="a34e6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a34e6-111">Value</span></span>                                                                                        | <span data-ttu-id="a34e6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a34e6-112">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a34e6-113"><dt>фирстплай</dt></span><span class="sxs-lookup"><span data-stu-id="a34e6-113"><dt>firstPlay</dt></span></span> </dl>         | <span data-ttu-id="a34e6-114">Выполнение инициализации DVD-диска по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a34e6-114">Performing default initialization of a DVD disc.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="a34e6-115"><dt>видеоманажермену</dt></span><span class="sxs-lookup"><span data-stu-id="a34e6-115"><dt>videoManagerMenu</dt></span></span> </dl>  | <span data-ttu-id="a34e6-116">Отображение меню для всего диска. Также известен как Топмену для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a34e6-116">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="a34e6-117">Обычно называется меню заголовка или верхним меню.</span><span class="sxs-lookup"><span data-stu-id="a34e6-117">Commonly called the title menu or the top menu.</span></span><br/> |
| <dl> <span data-ttu-id="a34e6-118"><dt>видеотитлесетмену</dt></span><span class="sxs-lookup"><span data-stu-id="a34e6-118"><dt>videoTitleSetMenu</dt></span></span> </dl> | <span data-ttu-id="a34e6-119">Отображение меню для текущего набора заголовков.</span><span class="sxs-lookup"><span data-stu-id="a34e6-119">Displaying menus for the current title set.</span></span> <span data-ttu-id="a34e6-120">Также известен как Титлемену для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a34e6-120">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="a34e6-121">Обычно называется корневым меню.</span><span class="sxs-lookup"><span data-stu-id="a34e6-121">Commonly called the root menu.</span></span><br/>          |
| <dl> <span data-ttu-id="a34e6-122"><dt>title</dt></span><span class="sxs-lookup"><span data-stu-id="a34e6-122"><dt>title</dt></span></span> </dl>             | <span data-ttu-id="a34e6-123">Обычно отображение текущего заголовка.</span><span class="sxs-lookup"><span data-stu-id="a34e6-123">Usually, displaying the current title.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="a34e6-124"><dt>stop</dt></span><span class="sxs-lookup"><span data-stu-id="a34e6-124"><dt>stop</dt></span></span> </dl>              | <span data-ttu-id="a34e6-125">Навигатор DVD находится в области DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="a34e6-125">The DVD Navigator is in the DVD Stop domain.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="a34e6-126"><dt>определено</dt></span><span class="sxs-lookup"><span data-stu-id="a34e6-126"><dt>undefined</dt></span></span> </dl>         | <span data-ttu-id="a34e6-127">Проигрыватель Windows Media не находится ни в одном DVD-домене.</span><span class="sxs-lookup"><span data-stu-id="a34e6-127">Windows Media Player is not in any DVD domain.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="a34e6-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a34e6-128">Remarks</span></span>

<span data-ttu-id="a34e6-129">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="a34e6-129">Every DVD is authored differently.</span></span> <span data-ttu-id="a34e6-130">Некоторые DVD-диски не содержат домены Фирстплай, Видеоманажермену или Видеотитлесетмену.</span><span class="sxs-lookup"><span data-stu-id="a34e6-130">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="a34e6-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a34e6-131">Requirements</span></span>



| <span data-ttu-id="a34e6-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a34e6-132">Requirement</span></span> | <span data-ttu-id="a34e6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a34e6-133">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34e6-134">Версия</span><span class="sxs-lookup"><span data-stu-id="a34e6-134">Version</span></span><br/>   | <span data-ttu-id="a34e6-135">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a34e6-135">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a34e6-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a34e6-136">Namespace</span></span><br/> | <span data-ttu-id="a34e6-137">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="a34e6-137">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a34e6-138">Сборка</span><span class="sxs-lookup"><span data-stu-id="a34e6-138">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a34e6-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a34e6-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a34e6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a34e6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a34e6-141">**Интерфейс ИВМПДВД (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a34e6-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





