---
title: ИВМПДВД Топмену, метод
description: Метод Топмену останавливает воспроизведение и отображает верхнее (или корневое) меню для текущего заголовка.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- Топмену метод Windows Media Player
- Топмену метод проигрывателя Windows Media Player, интерфейс ИВМПДВД
- Интерфейс ИВМПДВД Windows Media Player, метод Топмену
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718123"
---
# <a name="iwmpdvdtopmenu-method"></a><span data-ttu-id="cf199-106">Метод ИВМПДВД:: Топмену</span><span class="sxs-lookup"><span data-stu-id="cf199-106">IWMPDVD::topMenu method</span></span>

<span data-ttu-id="cf199-107">Метод **топмену** останавливает воспроизведение и отображает верхнее (или корневое) меню для текущего заголовка.</span><span class="sxs-lookup"><span data-stu-id="cf199-107">The **topMenu** method stops playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf199-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf199-108">Syntax</span></span>


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a><span data-ttu-id="cf199-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf199-109">Parameters</span></span>

<span data-ttu-id="cf199-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cf199-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf199-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf199-111">Return value</span></span>

<span data-ttu-id="cf199-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cf199-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf199-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf199-113">Remarks</span></span>

<span data-ttu-id="cf199-114">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="cf199-114">Every DVD is authored differently.</span></span> <span data-ttu-id="cf199-115">Чтобы этот метод работал, DVD-диск должен содержать меню.</span><span class="sxs-lookup"><span data-stu-id="cf199-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="cf199-116">Некоторые DVD-диски созданы таким образом, чтобы методы **топмену** и **ивмпдвд. титлемену** открывали одно и то же меню.</span><span class="sxs-lookup"><span data-stu-id="cf199-116">Some DVDs are authored so that the **topMenu** and **IWMPDVD.titleMenu** methods open the same menu.</span></span> <span data-ttu-id="cf199-117">Метод **топмену** обычно вызывает верхнее (или корневое) меню, но может вызвать меню заголовка, если нет доступного корневого меню.</span><span class="sxs-lookup"><span data-stu-id="cf199-117">The **topMenu** method usually invokes the top (or root) menu, but it may invoke the title menu if there is no root menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf199-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cf199-118">Requirements</span></span>



| <span data-ttu-id="cf199-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cf199-119">Requirement</span></span> | <span data-ttu-id="cf199-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cf199-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf199-121">Версия</span><span class="sxs-lookup"><span data-stu-id="cf199-121">Version</span></span><br/>   | <span data-ttu-id="cf199-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="cf199-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cf199-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf199-123">Namespace</span></span><br/> | <span data-ttu-id="cf199-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="cf199-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cf199-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="cf199-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cf199-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cf199-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf199-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf199-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf199-128">**Интерфейс ИВМПДВД (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cf199-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf199-129">**ИВМПДВД. Титлемену (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cf199-129">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





