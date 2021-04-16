---
title: Клоседкаптион. Жетсамилангид, метод
description: Метод Жетсамилангид извлекает идентификатор локали (LCID) языка, поддерживаемого текущим файлом SAMI.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- Жетсамилангид метод Windows Media Player
- Жетсамилангид метод Windows Media Player, класс Клоседкаптион
- Класс Клоседкаптион Windows Media Player, метод Жетсамилангид
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699291"
---
# <a name="closedcaptiongetsamilangid-method"></a><span data-ttu-id="8c15c-106">Клоседкаптион. Жетсамилангид, метод</span><span class="sxs-lookup"><span data-stu-id="8c15c-106">ClosedCaption.getSAMILangID method</span></span>

<span data-ttu-id="8c15c-107">Метод **жетсамилангид** извлекает идентификатор локали (LCID) языка, поддерживаемого текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="8c15c-107">The **getSAMILangID** method retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c15c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c15c-108">Syntax</span></span>


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="8c15c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c15c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c15c-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c15c-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c15c-111">**Число** (**Long**), указывающее индекс извлекаемого кода языка.</span><span class="sxs-lookup"><span data-stu-id="8c15c-111">**Number** (**long**) specifying the index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c15c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c15c-112">Return value</span></span>

<span data-ttu-id="8c15c-113">Этот метод возвращает **число** (**Long**), содержащее LCID языка с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="8c15c-113">This method returns a **Number** (**long**) containing the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c15c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c15c-114">Remarks</span></span>

<span data-ttu-id="8c15c-115">Языки в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.</span><span class="sxs-lookup"><span data-stu-id="8c15c-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="8c15c-116">Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).</span><span class="sxs-lookup"><span data-stu-id="8c15c-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="8c15c-117">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8c15c-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c15c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8c15c-118">Requirements</span></span>



| <span data-ttu-id="8c15c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8c15c-119">Requirement</span></span> | <span data-ttu-id="8c15c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8c15c-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c15c-121">Версия</span><span class="sxs-lookup"><span data-stu-id="8c15c-121">Version</span></span><br/> | <span data-ttu-id="8c15c-122">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="8c15c-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="8c15c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8c15c-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c15c-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c15c-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c15c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c15c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c15c-126">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="8c15c-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="8c15c-127">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="8c15c-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





