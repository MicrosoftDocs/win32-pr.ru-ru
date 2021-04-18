---
title: Клоседкаптион. Жетсамистиленаме, метод
description: Метод Жетсамистиленаме извлекает имя стиля, поддерживаемого текущим файлом SAMI.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- Жетсамистиленаме метод Windows Media Player
- Жетсамистиленаме метод Windows Media Player, класс Клоседкаптион
- Класс Клоседкаптион Windows Media Player, метод Жетсамистиленаме
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694876"
---
# <a name="closedcaptiongetsamistylename-method"></a><span data-ttu-id="8a1bb-106">Клоседкаптион. Жетсамистиленаме, метод</span><span class="sxs-lookup"><span data-stu-id="8a1bb-106">ClosedCaption.getSAMIStyleName method</span></span>

<span data-ttu-id="8a1bb-107">Метод **жетсамистиленаме** извлекает имя стиля, поддерживаемого текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="8a1bb-107">The **getSAMIStyleName** method retrieves the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a1bb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a1bb-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="8a1bb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a1bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a1bb-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a1bb-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1bb-111">**Число** (**длинное**), определяющее индекс извлекаемого имени стиля.</span><span class="sxs-lookup"><span data-stu-id="8a1bb-111">**Number** (**long**) specifying the index of the style name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a1bb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a1bb-112">Return value</span></span>

<span data-ttu-id="8a1bb-113">Этот метод возвращает **строку** , содержащую имя стиля, как указано в файле Sami.</span><span class="sxs-lookup"><span data-stu-id="8a1bb-113">This method returns a **String** containing the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a1bb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a1bb-114">Remarks</span></span>

<span data-ttu-id="8a1bb-115">Стили в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.</span><span class="sxs-lookup"><span data-stu-id="8a1bb-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="8a1bb-116">Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).</span><span class="sxs-lookup"><span data-stu-id="8a1bb-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="8a1bb-117">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8a1bb-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a1bb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8a1bb-118">Requirements</span></span>



| <span data-ttu-id="8a1bb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8a1bb-119">Requirement</span></span> | <span data-ttu-id="8a1bb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8a1bb-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1bb-121">Версия</span><span class="sxs-lookup"><span data-stu-id="8a1bb-121">Version</span></span><br/> | <span data-ttu-id="8a1bb-122">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="8a1bb-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="8a1bb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8a1bb-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="8a1bb-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a1bb-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a1bb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a1bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1bb-126">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="8a1bb-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="8a1bb-127">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="8a1bb-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="8a1bb-128">**Клоседкаптион. Самистиле**</span><span class="sxs-lookup"><span data-stu-id="8a1bb-128">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





