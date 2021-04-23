---
title: Ивмпкдромбурн доступный метод
description: Метод Available предоставляет сведения о дисководе компакт-дисков и носителях.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- метод Available проигрыватель Windows Media Player
- метод Available проигрыватель Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод Available
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717980"
---
# <a name="iwmpcdromburnisavailable-method"></a><span data-ttu-id="67943-106">Метод Ивмпкдромбурн:: Available</span><span class="sxs-lookup"><span data-stu-id="67943-106">IWMPCdromBurn::isAvailable method</span></span>

<span data-ttu-id="67943-107">Метод **Available** предоставляет сведения о ДИСКОВОДЕ компакт-дисков и носителях.</span><span class="sxs-lookup"><span data-stu-id="67943-107">The **isAvailable** method provides information about the CD drive and media.</span></span>

## <a name="syntax"></a><span data-ttu-id="67943-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67943-108">Syntax</span></span>


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a><span data-ttu-id="67943-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="67943-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67943-110">*бстритем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67943-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67943-111">**Строка System. String** , которая содержит одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="67943-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="67943-112">Значение</span><span class="sxs-lookup"><span data-stu-id="67943-112">Value</span></span> | <span data-ttu-id="67943-113">Описание</span><span class="sxs-lookup"><span data-stu-id="67943-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="67943-114">Записать</span><span class="sxs-lookup"><span data-stu-id="67943-114">Burn</span></span>  | <span data-ttu-id="67943-115">Диск является устройством записи компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="67943-115">The drive is a CD burner.</span></span>   |
| <span data-ttu-id="67943-116">Корр</span><span class="sxs-lookup"><span data-stu-id="67943-116">Disc</span></span>  | <span data-ttu-id="67943-117">В дисководе есть компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="67943-117">There is a CD in the drive.</span></span> |
| <span data-ttu-id="67943-118">Очистка</span><span class="sxs-lookup"><span data-stu-id="67943-118">Erase</span></span> | <span data-ttu-id="67943-119">Компакт-диск можно стереть.</span><span class="sxs-lookup"><span data-stu-id="67943-119">The CD can be erased.</span></span>       |
| <span data-ttu-id="67943-120">запись</span><span class="sxs-lookup"><span data-stu-id="67943-120">Write</span></span> | <span data-ttu-id="67943-121">Компакт-диск можно записать в.</span><span class="sxs-lookup"><span data-stu-id="67943-121">The CD can be written to.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67943-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67943-122">Return value</span></span>

<span data-ttu-id="67943-123">Значение **System. Boolean** , указывающее результат.</span><span class="sxs-lookup"><span data-stu-id="67943-123">A **System.Boolean** that indicates the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="67943-124">Требования</span><span class="sxs-lookup"><span data-stu-id="67943-124">Requirements</span></span>



| <span data-ttu-id="67943-125">Требование</span><span class="sxs-lookup"><span data-stu-id="67943-125">Requirement</span></span> | <span data-ttu-id="67943-126">Значение</span><span class="sxs-lookup"><span data-stu-id="67943-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67943-127">Версия</span><span class="sxs-lookup"><span data-stu-id="67943-127">Version</span></span><br/>   | <span data-ttu-id="67943-128">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="67943-128">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="67943-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="67943-129">Namespace</span></span><br/> | <span data-ttu-id="67943-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="67943-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="67943-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="67943-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="67943-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="67943-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67943-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67943-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67943-134">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="67943-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





