---
title: Список воспроизведения. копирование
description: Метод Copy начинает операцию копирования с компакт-диска.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- Список воспроизведения. копирование проигрывателя Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704445"
---
# <a name="playlistcopy"></a><span data-ttu-id="dad24-104">Список воспроизведения. копирование</span><span class="sxs-lookup"><span data-stu-id="dad24-104">PLAYLIST.copy</span></span>

<span data-ttu-id="dad24-105">Метод **Copy** начинает операцию копирования с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="dad24-105">The **copy** method begins a copy operation from the CD.</span></span>

``` syntax
        elementID.copy()
```

## <a name="parameters"></a><span data-ttu-id="dad24-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dad24-106">Parameters</span></span>

<span data-ttu-id="dad24-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dad24-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dad24-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dad24-108">Return Value</span></span>

<span data-ttu-id="dad24-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dad24-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dad24-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dad24-110">Remarks</span></span>

<span data-ttu-id="dad24-111">Этот метод копирует только отмеченные элементы в списке воспроизведения и работает так же, как и на панели **копирование с компакт-диска** в полноэкранном режиме проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dad24-111">This method copies only the checked items in the playlist, and works the same way as in the **Copy from CD** pane in the full mode of Windows Media Player.</span></span> <span data-ttu-id="dad24-112">Чтобы этот метод работал, компакт-диск должен находиться в дисководе компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="dad24-112">For this method to work, a CD must be in the CD drive.</span></span> <span data-ttu-id="dad24-113">Присвойте атрибуту **чеккбоксесвисибле** значение true, чтобы разрешить пользователям выбирать отдельные элементы на компакт-диске перед копированием.</span><span class="sxs-lookup"><span data-stu-id="dad24-113">Set the **checkboxesVisible** attribute to true to allow users to select individual items on a CD before copying.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad24-114">Требования</span><span class="sxs-lookup"><span data-stu-id="dad24-114">Requirements</span></span>



| <span data-ttu-id="dad24-115">Требование</span><span class="sxs-lookup"><span data-stu-id="dad24-115">Requirement</span></span> | <span data-ttu-id="dad24-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dad24-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="dad24-117">Версия</span><span class="sxs-lookup"><span data-stu-id="dad24-117">Version</span></span><br/> | <span data-ttu-id="dad24-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="dad24-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dad24-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dad24-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad24-120">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="dad24-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="dad24-121">**Список воспроизведения. Аборткопи**</span><span class="sxs-lookup"><span data-stu-id="dad24-121">**PLAYLIST.abortCopy**</span></span>](playlist-abortcopy.md)
</dt> <dt>

[<span data-ttu-id="dad24-122">**Список воспроизведения. копирование**</span><span class="sxs-lookup"><span data-stu-id="dad24-122">**PLAYLIST.copying**</span></span>](playlist-copying.md)
</dt> </dl>

 

 





