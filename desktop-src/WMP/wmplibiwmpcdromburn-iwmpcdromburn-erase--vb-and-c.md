---
title: Ивмпкдромбурн, метод erase
description: Метод Erase стирает текущий компакт-диск.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- Стирание метода проигрывателя Windows Media Player
- Стирание метода проигрыватель Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717983"
---
# <a name="iwmpcdromburnerase-method"></a><span data-ttu-id="1d130-106">Метод Ивмпкдромбурн:: Erase</span><span class="sxs-lookup"><span data-stu-id="1d130-106">IWMPCdromBurn::erase method</span></span>

<span data-ttu-id="1d130-107">Метод **Erase** стирает текущий компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="1d130-107">The **erase** method erases the current CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d130-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d130-108">Syntax</span></span>


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a><span data-ttu-id="1d130-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d130-109">Parameters</span></span>

<span data-ttu-id="1d130-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1d130-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d130-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d130-111">Return value</span></span>

<span data-ttu-id="1d130-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1d130-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d130-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d130-113">Remarks</span></span>

<span data-ttu-id="1d130-114">Этот метод не будет работать, если диск в устройстве не может быть перезаписываемым.</span><span class="sxs-lookup"><span data-stu-id="1d130-114">This method will not work if the disc in the drive is not rewritable.</span></span> <span data-ttu-id="1d130-115">Используйте [ивмпкдромбурн. Available](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) , чтобы определить, можно ли стереть компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="1d130-115">Use [IWMPCdromBurn.isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) to determine whether a CD can be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d130-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1d130-116">Requirements</span></span>



| <span data-ttu-id="1d130-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1d130-117">Requirement</span></span> | <span data-ttu-id="1d130-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1d130-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d130-119">Версия</span><span class="sxs-lookup"><span data-stu-id="1d130-119">Version</span></span><br/>   | <span data-ttu-id="1d130-120">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="1d130-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="1d130-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d130-121">Namespace</span></span><br/> | <span data-ttu-id="1d130-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="1d130-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1d130-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="1d130-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1d130-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1d130-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d130-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d130-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d130-126">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1d130-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





