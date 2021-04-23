---
title: Controls. Жетлангуаженаме, метод
description: Метод Жетлангуаженаме извлекает имя звукового языка с указанным кодом локали (LCID).
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- Жетлангуаженаме метод Windows Media Player
- метод Жетлангуаженаме Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Жетлангуаженаме
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698901"
---
# <a name="controlsgetlanguagename-method"></a><span data-ttu-id="87905-106">Controls. Жетлангуаженаме, метод</span><span class="sxs-lookup"><span data-stu-id="87905-106">Controls.getLanguageName method</span></span>

<span data-ttu-id="87905-107">Метод **жетлангуаженаме** извлекает имя звукового языка с указанным кодом локали (LCID).</span><span class="sxs-lookup"><span data-stu-id="87905-107">The **getLanguageName** method retrieves the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="87905-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87905-108">Syntax</span></span>


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a><span data-ttu-id="87905-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="87905-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87905-110">*Код языка* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="87905-110">*LCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87905-111">**Число** (**длинное**), определяющее код языка.</span><span class="sxs-lookup"><span data-stu-id="87905-111">**Number** (**long**) specifying the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87905-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87905-112">Return value</span></span>

<span data-ttu-id="87905-113">Этот метод возвращает **строку**.</span><span class="sxs-lookup"><span data-stu-id="87905-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="87905-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87905-114">Remarks</span></span>

<span data-ttu-id="87905-115">Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="87905-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="87905-116">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="87905-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="87905-117">Требования</span><span class="sxs-lookup"><span data-stu-id="87905-117">Requirements</span></span>



| <span data-ttu-id="87905-118">Требование</span><span class="sxs-lookup"><span data-stu-id="87905-118">Requirement</span></span> | <span data-ttu-id="87905-119">Значение</span><span class="sxs-lookup"><span data-stu-id="87905-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87905-120">Версия</span><span class="sxs-lookup"><span data-stu-id="87905-120">Version</span></span><br/> | <span data-ttu-id="87905-121">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="87905-121">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="87905-122">DLL</span><span class="sxs-lookup"><span data-stu-id="87905-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="87905-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87905-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87905-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87905-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87905-125">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="87905-125">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="87905-126">**Controls. Аудиолангуажекаунт**</span><span class="sxs-lookup"><span data-stu-id="87905-126">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="87905-127">**Controls. Куррентаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="87905-127">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="87905-128">**Controls. Куррентаудиолангуажеиндекс**</span><span class="sxs-lookup"><span data-stu-id="87905-128">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="87905-129">**Controls. Жетаудиолангуажедескриптион**</span><span class="sxs-lookup"><span data-stu-id="87905-129">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="87905-130">**Controls. Жетаудиолангуажеид**</span><span class="sxs-lookup"><span data-stu-id="87905-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





