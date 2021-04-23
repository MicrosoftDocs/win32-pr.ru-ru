---
title: ИВМПДВД Титлемену, метод
description: Метод Титлемену останавливает воспроизведение и отображает меню заголовка.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- Титлемену метод Windows Media Player
- Титлемену метод проигрывателя Windows Media Player, интерфейс ИВМПДВД
- Интерфейс ИВМПДВД Windows Media Player, метод Титлемену
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657941"
---
# <a name="iwmpdvdtitlemenu-method"></a><span data-ttu-id="9e330-106">Метод ИВМПДВД:: Титлемену</span><span class="sxs-lookup"><span data-stu-id="9e330-106">IWMPDVD::titleMenu method</span></span>

<span data-ttu-id="9e330-107">Метод **титлемену** останавливает воспроизведение и отображает меню заголовка.</span><span class="sxs-lookup"><span data-stu-id="9e330-107">The **titleMenu** method stops playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e330-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e330-108">Syntax</span></span>


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a><span data-ttu-id="9e330-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e330-109">Parameters</span></span>

<span data-ttu-id="9e330-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9e330-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e330-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e330-111">Return value</span></span>

<span data-ttu-id="9e330-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9e330-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e330-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e330-113">Remarks</span></span>

<span data-ttu-id="9e330-114">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="9e330-114">Every DVD is authored differently.</span></span> <span data-ttu-id="9e330-115">Чтобы этот метод работал, DVD-диск должен содержать меню.</span><span class="sxs-lookup"><span data-stu-id="9e330-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="9e330-116">Некоторые DVD-диски созданы таким образом, чтобы методы **ивмпдвд. топмену** и **титлемену** открывали одно и то же меню.</span><span class="sxs-lookup"><span data-stu-id="9e330-116">Some DVDs are authored so that the **IWMPDVD.topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="9e330-117">Метод **титлемену** обычно вызывает меню заголовка, но он может вызвать верхнее меню, если нет доступного меню заголовка.</span><span class="sxs-lookup"><span data-stu-id="9e330-117">The **titleMenu** method usually invokes the title menu, but it may invoke the top menu if there is no title menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e330-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9e330-118">Requirements</span></span>



| <span data-ttu-id="9e330-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9e330-119">Requirement</span></span> | <span data-ttu-id="9e330-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9e330-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e330-121">Версия</span><span class="sxs-lookup"><span data-stu-id="9e330-121">Version</span></span><br/>   | <span data-ttu-id="9e330-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9e330-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9e330-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9e330-123">Namespace</span></span><br/> | <span data-ttu-id="9e330-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="9e330-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9e330-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="9e330-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9e330-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9e330-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e330-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e330-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e330-128">**Интерфейс ИВМПДВД (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9e330-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9e330-129">**ИВМПДВД. Топмену (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9e330-129">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





