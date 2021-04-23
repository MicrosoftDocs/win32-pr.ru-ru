---
title: Клоседкаптион. Самистилекаунт
description: Свойство Самистилекаунт извлекает количество стилей, поддерживаемое текущим файлом SAMI.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самистилекаунт
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694560"
---
# <a name="closedcaptionsamistylecount"></a><span data-ttu-id="f5b69-104">Клоседкаптион. Самистилекаунт</span><span class="sxs-lookup"><span data-stu-id="f5b69-104">ClosedCaption.SAMIStyleCount</span></span>

<span data-ttu-id="f5b69-105">Свойство **самистилекаунт** извлекает количество стилей, поддерживаемое текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="f5b69-105">The **SAMIStyleCount** property retrieves the number of styles supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a><span data-ttu-id="f5b69-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f5b69-106">Possible Values</span></span>

<span data-ttu-id="f5b69-107">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="f5b69-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b69-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5b69-108">Remarks</span></span>

<span data-ttu-id="f5b69-109">Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).</span><span class="sxs-lookup"><span data-stu-id="f5b69-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="f5b69-110">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="f5b69-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b69-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f5b69-111">Requirements</span></span>



| <span data-ttu-id="f5b69-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f5b69-112">Requirement</span></span> | <span data-ttu-id="f5b69-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f5b69-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b69-114">Версия</span><span class="sxs-lookup"><span data-stu-id="f5b69-114">Version</span></span><br/> | <span data-ttu-id="f5b69-115">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f5b69-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f5b69-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b69-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="f5b69-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b69-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5b69-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5b69-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b69-119">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="f5b69-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f5b69-120">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="f5b69-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="f5b69-121">**Клоседкаптион. Жетсамистиленаме**</span><span class="sxs-lookup"><span data-stu-id="f5b69-121">**ClosedCaption.getSAMIStyleName**</span></span>](closedcaption-getsamistylename.md)
</dt> <dt>

[<span data-ttu-id="f5b69-122">**Клоседкаптион. Самистиле**</span><span class="sxs-lookup"><span data-stu-id="f5b69-122">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





