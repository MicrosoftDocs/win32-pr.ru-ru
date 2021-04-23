---
title: Ивмпкдромбурн Стартбурн, метод
description: Метод Стартбурн записывает компакт-диск.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- Стартбурн метод Windows Media Player
- Стартбурн метод проигрывателя Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод Стартбурн
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717976"
---
# <a name="iwmpcdromburnstartburn-method"></a><span data-ttu-id="93fc4-106">Метод Ивмпкдромбурн:: Стартбурн</span><span class="sxs-lookup"><span data-stu-id="93fc4-106">IWMPCdromBurn::startBurn method</span></span>

<span data-ttu-id="93fc4-107">Метод **стартбурн** записывает компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="93fc4-107">The **startBurn** method burns the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="93fc4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93fc4-108">Syntax</span></span>


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a><span data-ttu-id="93fc4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="93fc4-109">Parameters</span></span>

<span data-ttu-id="93fc4-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="93fc4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93fc4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93fc4-111">Return value</span></span>

<span data-ttu-id="93fc4-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="93fc4-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93fc4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93fc4-113">Remarks</span></span>

<span data-ttu-id="93fc4-114">Перед вызовом этого метода значение **бурнстате** должно быть Вмпбсреади или вмпбсстоппед.</span><span class="sxs-lookup"><span data-stu-id="93fc4-114">The value of **burnstate** should be wmpbsReady or wmpbsStopped before calling this method.</span></span>

<span data-ttu-id="93fc4-115">Этот метод не будет работать, если дисковод компакт-дисков не является устройством записи или диск не доступен для записи.</span><span class="sxs-lookup"><span data-stu-id="93fc4-115">This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable.</span></span> <span data-ttu-id="93fc4-116">Чтобы определить, можно ли записать компакт-диск, воспользуйтесь возможностью **доступа** .</span><span class="sxs-lookup"><span data-stu-id="93fc4-116">Use **isAvailable** to determine whether a CD can be burned.</span></span>

## <a name="requirements"></a><span data-ttu-id="93fc4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="93fc4-117">Requirements</span></span>



| <span data-ttu-id="93fc4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="93fc4-118">Requirement</span></span> | <span data-ttu-id="93fc4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="93fc4-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93fc4-120">Версия</span><span class="sxs-lookup"><span data-stu-id="93fc4-120">Version</span></span><br/>   | <span data-ttu-id="93fc4-121">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="93fc4-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="93fc4-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93fc4-122">Namespace</span></span><br/> | <span data-ttu-id="93fc4-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="93fc4-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="93fc4-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="93fc4-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="93fc4-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="93fc4-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93fc4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93fc4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93fc4-127">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="93fc4-127">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="93fc4-128">**Ивмпкдромбурн. Бурнстате (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="93fc4-128">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="93fc4-129">**Ивмпкдромбурн. доступ (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="93fc4-129">**IWMPCdromBurn.isAvailable (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="93fc4-130">**Ивмпкдромбурн. Стопбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="93fc4-130">**IWMPCdromBurn.stopBurn (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





