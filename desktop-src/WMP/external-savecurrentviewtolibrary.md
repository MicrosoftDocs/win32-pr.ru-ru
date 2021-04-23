---
title: External. Савекуррентвиевтолибрари, метод
description: Метод Савекуррентвиевтолибрари создает список воспроизведения из элементов мультимедиа в текущем представлении и сохраняет список воспроизведения в локальной библиотеке.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- Савекуррентвиевтолибрари метод Windows Media Player
- Савекуррентвиевтолибрари метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Савекуррентвиевтолибрари
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694485"
---
# <a name="externalsavecurrentviewtolibrary-method"></a><span data-ttu-id="ff944-106">External. Савекуррентвиевтолибрари, метод</span><span class="sxs-lookup"><span data-stu-id="ff944-106">External.saveCurrentViewToLibrary method</span></span>

<span data-ttu-id="ff944-107">Метод **савекуррентвиевтолибрари** создает список воспроизведения из элементов мультимедиа в текущем представлении и сохраняет список воспроизведения в локальной библиотеке.</span><span class="sxs-lookup"><span data-stu-id="ff944-107">The **saveCurrentViewToLibrary** method creates a playlist from the media items in the current view and saves the playlist in the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff944-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff944-108">Syntax</span></span>


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a><span data-ttu-id="ff944-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff944-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff944-110">*Фриендлилистнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff944-110">*FriendlyListName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff944-111">**Строка** , указывающая понятное имя для списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ff944-111">**String** that specifies a friendly name for the playlist.</span></span> <span data-ttu-id="ff944-112">Проигрыватель Windows Media отображает это имя в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ff944-112">Windows Media Player displays this name in its user interface.</span></span>

</dd> <dt>

<span data-ttu-id="ff944-113">*Локальный* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff944-113">*Local* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff944-114">**Логическое значение** , указывающее, является ли список воспроизведения динамическим или статическим.</span><span class="sxs-lookup"><span data-stu-id="ff944-114">**Boolean** that specifies whether the playlist is dynamic or static.</span></span> <span data-ttu-id="ff944-115">**Значение true** указывает Dynamic, а **false** — статический.</span><span class="sxs-lookup"><span data-stu-id="ff944-115">**TRUE** specifies dynamic, and **FALSE** specifies static.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff944-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff944-116">Return value</span></span>

<span data-ttu-id="ff944-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ff944-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff944-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ff944-118">Requirements</span></span>



| <span data-ttu-id="ff944-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ff944-119">Requirement</span></span> | <span data-ttu-id="ff944-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ff944-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff944-121">Версия</span><span class="sxs-lookup"><span data-stu-id="ff944-121">Version</span></span><br/> | <span data-ttu-id="ff944-122">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="ff944-122">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="ff944-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ff944-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ff944-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff944-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff944-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff944-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff944-126">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="ff944-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





