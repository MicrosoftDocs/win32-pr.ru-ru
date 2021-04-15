---
title: Клоседкаптион. Жетсамилангнаме, метод
description: Метод Жетсамилангнаме извлекает имя языка, поддерживаемого текущим файлом SAMI.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- Жетсамилангнаме метод Windows Media Player
- Жетсамилангнаме метод Windows Media Player, класс Клоседкаптион
- Класс Клоседкаптион Windows Media Player, метод Жетсамилангнаме
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695125"
---
# <a name="closedcaptiongetsamilangname-method"></a><span data-ttu-id="9c20b-106">Клоседкаптион. Жетсамилангнаме, метод</span><span class="sxs-lookup"><span data-stu-id="9c20b-106">ClosedCaption.getSAMILangName method</span></span>

<span data-ttu-id="9c20b-107">Метод **жетсамилангнаме** извлекает имя языка, поддерживаемого текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="9c20b-107">The **getSAMILangName** method retrieves the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c20b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c20b-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="9c20b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c20b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c20b-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c20b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c20b-111">**Число** (**длинное**), определяющее индекс имени языка для извлечения.</span><span class="sxs-lookup"><span data-stu-id="9c20b-111">**Number** (**long**) specifying the index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c20b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c20b-112">Return value</span></span>

<span data-ttu-id="9c20b-113">Этот метод возвращает **строку** , содержащую имя языка, указанное в файле Sami.</span><span class="sxs-lookup"><span data-stu-id="9c20b-113">This method returns a **String** containing the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c20b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c20b-114">Remarks</span></span>

<span data-ttu-id="9c20b-115">Языки в файле SAMI индексируются в порядке, указанном в файле, начиная с нуля.</span><span class="sxs-lookup"><span data-stu-id="9c20b-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="9c20b-116">Этот метод нельзя использовать до открытия файла цифрового мультимедиа (*Player*.**Опенстате** равен 13).</span><span class="sxs-lookup"><span data-stu-id="9c20b-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="9c20b-117">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c20b-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c20b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9c20b-118">Requirements</span></span>



| <span data-ttu-id="9c20b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9c20b-119">Requirement</span></span> | <span data-ttu-id="9c20b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9c20b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c20b-121">Версия</span><span class="sxs-lookup"><span data-stu-id="9c20b-121">Version</span></span><br/> | <span data-ttu-id="9c20b-122">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9c20b-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="9c20b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9c20b-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="9c20b-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c20b-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c20b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c20b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c20b-126">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="9c20b-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="9c20b-127">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="9c20b-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="9c20b-128">**Клоседкаптион. Самиланг**</span><span class="sxs-lookup"><span data-stu-id="9c20b-128">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





