---
title: Ивмпкдромбурн, свойство метки
description: Свойство Label получает строку метки тома компакт-диска.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- свойство метки проигрыватель Windows Media
- свойство метки проигрыватель Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, свойство Label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717978"
---
# <a name="iwmpcdromburnlabel-property"></a><span data-ttu-id="024ac-106">Ивмпкдромбурн:: Label, свойство</span><span class="sxs-lookup"><span data-stu-id="024ac-106">IWMPCdromBurn::label property</span></span>

<span data-ttu-id="024ac-107">Свойство *Label* получает строку метки тома компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="024ac-107">The *label* property gets the CD volume label string.</span></span>

<span data-ttu-id="024ac-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="024ac-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="024ac-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="024ac-109">Syntax</span></span>


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a><span data-ttu-id="024ac-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="024ac-110">Property value</span></span>

<span data-ttu-id="024ac-111">Строка **System. String** , которая является строкой метки тома.</span><span class="sxs-lookup"><span data-stu-id="024ac-111">A **System.String** that is the volume label string.</span></span>

## <a name="remarks"></a><span data-ttu-id="024ac-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="024ac-112">Remarks</span></span>

<span data-ttu-id="024ac-113">В связи с тем, как хранятся метки компакт-дисков, метка компакт-диска может быть короче длины указанной строки метки тома.</span><span class="sxs-lookup"><span data-stu-id="024ac-113">Due to the way CD labels are stored, the label of the CD may be shorter than the length of the specified volume label string.</span></span> <span data-ttu-id="024ac-114">Если длина строки превышает максимальную длину метки компакт-диска, текст будет обрезан.</span><span class="sxs-lookup"><span data-stu-id="024ac-114">If the string is longer than the maximum length of a CD label, the text will be truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="024ac-115">Требования</span><span class="sxs-lookup"><span data-stu-id="024ac-115">Requirements</span></span>



| <span data-ttu-id="024ac-116">Требование</span><span class="sxs-lookup"><span data-stu-id="024ac-116">Requirement</span></span> | <span data-ttu-id="024ac-117">Значение</span><span class="sxs-lookup"><span data-stu-id="024ac-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="024ac-118">Версия</span><span class="sxs-lookup"><span data-stu-id="024ac-118">Version</span></span><br/>   | <span data-ttu-id="024ac-119">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="024ac-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="024ac-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="024ac-120">Namespace</span></span><br/> | <span data-ttu-id="024ac-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="024ac-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="024ac-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="024ac-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="024ac-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="024ac-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024ac-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="024ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024ac-125">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="024ac-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





