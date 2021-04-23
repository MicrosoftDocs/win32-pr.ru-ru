---
title: Клоседкаптион. Самилангкаунт
description: Свойство Самилангкаунт извлекает количество языков, поддерживаемых текущим файлом SAMI.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самилангкаунт
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694872"
---
# <a name="closedcaptionsamilangcount"></a><span data-ttu-id="9ca9c-104">Клоседкаптион. Самилангкаунт</span><span class="sxs-lookup"><span data-stu-id="9ca9c-104">ClosedCaption.SAMILangCount</span></span>

<span data-ttu-id="9ca9c-105">Свойство **самилангкаунт** извлекает количество языков, поддерживаемых текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="9ca9c-105">The **SAMILangCount** property retrieves the number of languages supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a><span data-ttu-id="9ca9c-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="9ca9c-106">Possible Values</span></span>

<span data-ttu-id="9ca9c-107">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="9ca9c-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca9c-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ca9c-108">Remarks</span></span>

<span data-ttu-id="9ca9c-109">Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).</span><span class="sxs-lookup"><span data-stu-id="9ca9c-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="9ca9c-110">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="9ca9c-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca9c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9ca9c-111">Requirements</span></span>



| <span data-ttu-id="9ca9c-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9ca9c-112">Requirement</span></span> | <span data-ttu-id="9ca9c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca9c-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca9c-114">Версия</span><span class="sxs-lookup"><span data-stu-id="9ca9c-114">Version</span></span><br/> | <span data-ttu-id="9ca9c-115">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9ca9c-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="9ca9c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="9ca9c-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ca9c-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ca9c-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca9c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ca9c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca9c-119">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="9ca9c-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="9ca9c-120">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="9ca9c-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="9ca9c-121">**Клоседкаптион. Жетсамилангнаме**</span><span class="sxs-lookup"><span data-stu-id="9ca9c-121">**ClosedCaption.getSAMILangName**</span></span>](closedcaption-getsamilangname.md)
</dt> <dt>

[<span data-ttu-id="9ca9c-122">**Клоседкаптион. Самиланг**</span><span class="sxs-lookup"><span data-stu-id="9ca9c-122">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





