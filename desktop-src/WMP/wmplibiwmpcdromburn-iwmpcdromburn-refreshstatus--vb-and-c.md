---
title: Ивмпкдромбурн Рефрешстатус, метод
description: Метод Рефрешстатус обновляет сведения о состоянии текущего списка воспроизведения записи.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- Рефрешстатус метод Windows Media Player
- Рефрешстатус метод проигрывателя Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод Рефрешстатус
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717977"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a><span data-ttu-id="99e82-106">Метод Ивмпкдромбурн:: Рефрешстатус</span><span class="sxs-lookup"><span data-stu-id="99e82-106">IWMPCdromBurn::refreshStatus method</span></span>

<span data-ttu-id="99e82-107">Метод **рефрешстатус** обновляет сведения о состоянии текущего списка воспроизведения записи.</span><span class="sxs-lookup"><span data-stu-id="99e82-107">The **refreshStatus** method updates the status information for the current burn playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e82-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99e82-108">Syntax</span></span>


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a><span data-ttu-id="99e82-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="99e82-109">Parameters</span></span>

<span data-ttu-id="99e82-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="99e82-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99e82-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99e82-111">Return value</span></span>

<span data-ttu-id="99e82-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="99e82-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e82-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99e82-113">Remarks</span></span>

<span data-ttu-id="99e82-114">Этот метод следует вызывать после создания или изменения списка воспроизведения записи перед чтением сведений о состоянии или записи компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="99e82-114">You should call this method after you create or change a burn playlist before reading status information or burning the CD.</span></span> <span data-ttu-id="99e82-115">Чтобы проверить, требуется ли обновление, получите значение **бурнстате** и проверьте наличие вмпбсрефрешстатуспендинг.</span><span class="sxs-lookup"><span data-stu-id="99e82-115">You can test whether a refresh is required by getting the value of **burnState** and checking for wmpbsRefreshStatusPending.</span></span>

<span data-ttu-id="99e82-116">Обновление состояния — это синхронная операция.</span><span class="sxs-lookup"><span data-stu-id="99e82-116">Refreshing the status is a synchronous operation.</span></span> <span data-ttu-id="99e82-117">Это означает, что длительный период времени может пройти, прежде чем этот метод возвратит значение, если текущий список воспроизведения имеет большой размер и содержит много изменений.</span><span class="sxs-lookup"><span data-stu-id="99e82-117">This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="99e82-118">Требования</span><span class="sxs-lookup"><span data-stu-id="99e82-118">Requirements</span></span>



| <span data-ttu-id="99e82-119">Требование</span><span class="sxs-lookup"><span data-stu-id="99e82-119">Requirement</span></span> | <span data-ttu-id="99e82-120">Значение</span><span class="sxs-lookup"><span data-stu-id="99e82-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e82-121">Версия</span><span class="sxs-lookup"><span data-stu-id="99e82-121">Version</span></span><br/>   | <span data-ttu-id="99e82-122">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="99e82-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="99e82-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="99e82-123">Namespace</span></span><br/> | <span data-ttu-id="99e82-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="99e82-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="99e82-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="99e82-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="99e82-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="99e82-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99e82-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99e82-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e82-128">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="99e82-128">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="99e82-129">**Ивмпкдромбурн. Бурнстате (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="99e82-129">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="99e82-130">**вмпбурнстате**</span><span class="sxs-lookup"><span data-stu-id="99e82-130">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





