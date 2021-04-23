---
title: Метод обратной передачи ИВМПДВД
description: Метод Back изменяет отображение из подменю на его родительское меню.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- метод обратной передачи Windows Media Player
- метод обратной передачи Windows Media Player, интерфейс ИВМПДВД
- Интерфейс ИВМПДВД Windows Media Player, метод Back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657943"
---
# <a name="iwmpdvdback-method"></a><span data-ttu-id="4c2dc-106">Метод ИВМПДВД:: Back</span><span class="sxs-lookup"><span data-stu-id="4c2dc-106">IWMPDVD::back method</span></span>

<span data-ttu-id="4c2dc-107">Метод **Back** изменяет отображение из подменю на его родительское меню.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-107">The **back** method changes the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c2dc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c2dc-108">Syntax</span></span>


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a><span data-ttu-id="4c2dc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c2dc-109">Parameters</span></span>

<span data-ttu-id="4c2dc-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c2dc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c2dc-111">Return value</span></span>

<span data-ttu-id="4c2dc-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c2dc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c2dc-113">Remarks</span></span>

<span data-ttu-id="4c2dc-114">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-114">Every DVD is authored differently.</span></span> <span data-ttu-id="4c2dc-115">Некоторые DVD-диски созданы таким образом, чтобы `back` метод был доступен из корневого меню, но при его вызове ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="4c2dc-115">Some DVDs are authored so that the `back` method is available from the root menu, but when invoked, it will do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c2dc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4c2dc-116">Requirements</span></span>



| <span data-ttu-id="4c2dc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4c2dc-117">Requirement</span></span> | <span data-ttu-id="4c2dc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4c2dc-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2dc-119">Версия</span><span class="sxs-lookup"><span data-stu-id="4c2dc-119">Version</span></span><br/>   | <span data-ttu-id="4c2dc-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4c2dc-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4c2dc-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4c2dc-121">Namespace</span></span><br/> | <span data-ttu-id="4c2dc-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="4c2dc-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4c2dc-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="4c2dc-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4c2dc-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4c2dc-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c2dc-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c2dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c2dc-126">**Интерфейс ИВМПДВД (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4c2dc-126">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





