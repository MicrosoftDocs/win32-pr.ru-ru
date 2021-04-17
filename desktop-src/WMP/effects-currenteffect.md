---
title: EFFECTs. Куррентеффект
description: Атрибут Куррентеффект указывает или получает текущую визуализацию.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- Effect. Куррентеффект Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694715"
---
# <a name="effectscurrenteffect"></a><span data-ttu-id="000eb-104">EFFECTs. Куррентеффект</span><span class="sxs-lookup"><span data-stu-id="000eb-104">EFFECTS.currentEffect</span></span>

<span data-ttu-id="000eb-105">Атрибут **куррентеффект** указывает или получает текущую визуализацию.</span><span class="sxs-lookup"><span data-stu-id="000eb-105">The **currentEffect** attribute specifies or retrieves the current visualization.</span></span>

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a><span data-ttu-id="000eb-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="000eb-106">Possible Values</span></span>

<span data-ttu-id="000eb-107">Этот атрибут является **объектом**, предназначенным для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="000eb-107">This attribute is a read/write **object**.</span></span> <span data-ttu-id="000eb-108">Значение по умолчанию — первое визуализация в порядке создания.</span><span class="sxs-lookup"><span data-stu-id="000eb-108">The default value is the first visualization in the authoring order.</span></span> <span data-ttu-id="000eb-109">Если в обложке нет созданных визуализаций, по умолчанию используется первая визуализация в реестре.</span><span class="sxs-lookup"><span data-stu-id="000eb-109">If there are no visualizations authored in the skin, the default is the first visualization in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="000eb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="000eb-110">Remarks</span></span>

<span data-ttu-id="000eb-111">Этот объект можно использовать для доступа к пользовательским визуализациям, которые вы создали.</span><span class="sxs-lookup"><span data-stu-id="000eb-111">You can use this object to access custom visualizations you have created.</span></span> <span data-ttu-id="000eb-112">Например, можно предоставить свойство через интерфейс **IDispatch** в визуализации.</span><span class="sxs-lookup"><span data-stu-id="000eb-112">For example, you could expose a property through the **IDispatch** interface in your visualization.</span></span> <span data-ttu-id="000eb-113">Затем можно изменить значение свойства из обложки, сделав визуализацию текущим, а затем используя объект **куррентеффект** , чтобы задать новое значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="000eb-113">You can then change the property value from your skin by making your visualization the current effect, and then using the **currentEffect** object to set a new value for the property.</span></span> <span data-ttu-id="000eb-114">Например, если визуализация предоставляет свойство с именем backgroundColor, в следующем коде JScript задается новое значение:</span><span class="sxs-lookup"><span data-stu-id="000eb-114">For example, if your visualization exposes a property named backgroundColor, the following JScript code specifies a new value:</span></span>


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a><span data-ttu-id="000eb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="000eb-115">Requirements</span></span>



| <span data-ttu-id="000eb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="000eb-116">Requirement</span></span> | <span data-ttu-id="000eb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="000eb-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="000eb-118">Версия</span><span class="sxs-lookup"><span data-stu-id="000eb-118">Version</span></span><br/> | <span data-ttu-id="000eb-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="000eb-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="000eb-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="000eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000eb-121">**EFFECTs, элемент**</span><span class="sxs-lookup"><span data-stu-id="000eb-121">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="000eb-122">**EFFECTs. Куррентеффекттитле**</span><span class="sxs-lookup"><span data-stu-id="000eb-122">**EFFECTS.currentEffectTitle**</span></span>](effects-currenteffecttitle.md)
</dt> <dt>

[<span data-ttu-id="000eb-123">**EFFECTs. Куррентеффекттипе**</span><span class="sxs-lookup"><span data-stu-id="000eb-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





