---
title: Свойство баланса Ивмпсеттингс
description: Свойство Balance получает или задает текущее значение стерео баланса.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Свойство баланса проигрыватель Windows Media Player
- Свойство баланса проигрыватель Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Balance
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718029"
---
# <a name="iwmpsettingsbalance-property"></a><span data-ttu-id="03201-106">Свойство Ивмпсеттингс:: Balance</span><span class="sxs-lookup"><span data-stu-id="03201-106">IWMPSettings::balance property</span></span>

<span data-ttu-id="03201-107">Свойство **Balance** получает или задает текущее значение стерео баланса.</span><span class="sxs-lookup"><span data-stu-id="03201-107">The **balance** property gets or sets the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="03201-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03201-108">Syntax</span></span>


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="03201-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="03201-109">Property value</span></span>

<span data-ttu-id="03201-110">Значение **System. Int32** , которое является значением баланса.</span><span class="sxs-lookup"><span data-stu-id="03201-110">A **System.Int32** that is the balance value.</span></span> <span data-ttu-id="03201-111">Это значение может находиться в диапазоне от 100 до 100.</span><span class="sxs-lookup"><span data-stu-id="03201-111">This value can range from  100 to 100.</span></span> <span data-ttu-id="03201-112">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="03201-112">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="03201-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03201-113">Remarks</span></span>

<span data-ttu-id="03201-114">Нулевое значение указывает на то, что звук воспроизводится на равном томе как в левом, так и в правой канале.</span><span class="sxs-lookup"><span data-stu-id="03201-114">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="03201-115">Значение 100 указывает, что звук воспроизводится только в левом канале.</span><span class="sxs-lookup"><span data-stu-id="03201-115">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="03201-116">Значение 100 указывает, что звук воспроизводится только в правильном канале.</span><span class="sxs-lookup"><span data-stu-id="03201-116">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="03201-117">Требования</span><span class="sxs-lookup"><span data-stu-id="03201-117">Requirements</span></span>



| <span data-ttu-id="03201-118">Требование</span><span class="sxs-lookup"><span data-stu-id="03201-118">Requirement</span></span> | <span data-ttu-id="03201-119">Значение</span><span class="sxs-lookup"><span data-stu-id="03201-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03201-120">Версия</span><span class="sxs-lookup"><span data-stu-id="03201-120">Version</span></span><br/>   | <span data-ttu-id="03201-121">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="03201-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="03201-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03201-122">Namespace</span></span><br/> | <span data-ttu-id="03201-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="03201-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="03201-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="03201-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="03201-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="03201-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03201-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03201-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03201-127">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="03201-127">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





