---
title: Ивмпкдромрип Стартрип, метод
description: Метод Стартрип Рипс компакт-диска.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- Стартрип метод Windows Media Player
- Стартрип метод проигрывателя Windows Media Player, интерфейс Ивмпкдромрип
- Интерфейс Ивмпкдромрип Windows Media Player, метод Стартрип
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648826"
---
# <a name="iwmpcdromripstartrip-method"></a><span data-ttu-id="6190e-106">Метод Ивмпкдромрип:: Стартрип</span><span class="sxs-lookup"><span data-stu-id="6190e-106">IWMPCdromRip::startRip method</span></span>

<span data-ttu-id="6190e-107">Метод **стартрип** Рипс компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="6190e-107">The **startRip** method rips the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="6190e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6190e-108">Syntax</span></span>


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a><span data-ttu-id="6190e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6190e-109">Parameters</span></span>

<span data-ttu-id="6190e-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6190e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6190e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6190e-111">Return value</span></span>

<span data-ttu-id="6190e-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6190e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6190e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6190e-113">Remarks</span></span>

<span data-ttu-id="6190e-114">Копирование компакт-диска с помощью интерфейса **ивмпкдромрип** действует так же, как копирование музыки с помощью пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6190e-114">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="6190e-115">Скопированное содержимое автоматически добавляется в библиотеку в соответствии с предпочтениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="6190e-115">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="6190e-116">Дополнительные сведения о параметрах пользователя для копирования компакт-дисков см. в разделе "Копирование музыки с CD" в справке проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6190e-116">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

## <a name="requirements"></a><span data-ttu-id="6190e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6190e-117">Requirements</span></span>



| <span data-ttu-id="6190e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6190e-118">Requirement</span></span> | <span data-ttu-id="6190e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6190e-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6190e-120">Версия</span><span class="sxs-lookup"><span data-stu-id="6190e-120">Version</span></span><br/>   | <span data-ttu-id="6190e-121">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="6190e-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="6190e-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6190e-122">Namespace</span></span><br/> | <span data-ttu-id="6190e-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="6190e-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6190e-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="6190e-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6190e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6190e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6190e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6190e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6190e-127">**Интерфейс Ивмпкдромрип (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6190e-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6190e-128">**Ивмпкдромрип. Стоприп**</span><span class="sxs-lookup"><span data-stu-id="6190e-128">**IWMPCdromRip.stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6190e-129">**Копирование компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="6190e-129">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





