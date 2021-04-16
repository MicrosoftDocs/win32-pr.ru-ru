---
title: ЕКУАЛИЗЕРСЕТТИНГС. Некстпресет
description: Метод Некстпресет применяет следующую предустановку эквалайзера.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- Проигрыватель Windows Media ЕКУАЛИЗЕРСЕТТИНГС. Некстпресет
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699143"
---
# <a name="equalizersettingsnextpreset"></a><span data-ttu-id="d5d09-104">ЕКУАЛИЗЕРСЕТТИНГС. Некстпресет</span><span class="sxs-lookup"><span data-stu-id="d5d09-104">EQUALIZERSETTINGS.nextPreset</span></span>

<span data-ttu-id="d5d09-105">Метод **некстпресет** применяет следующую предустановку эквалайзера.</span><span class="sxs-lookup"><span data-stu-id="d5d09-105">The **nextPreset** method applies the next equalizer preset.</span></span>

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a><span data-ttu-id="d5d09-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5d09-106">Parameters</span></span>

<span data-ttu-id="d5d09-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d5d09-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5d09-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5d09-108">Return Value</span></span>

<span data-ttu-id="d5d09-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d5d09-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d09-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5d09-110">Remarks</span></span>

<span data-ttu-id="d5d09-111">Если текущая Предустановка является последней доступной, первая Предустановка становится текущей.</span><span class="sxs-lookup"><span data-stu-id="d5d09-111">If the current preset is the last one available, the first preset is made current.</span></span>

## <a name="examples"></a><span data-ttu-id="d5d09-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="d5d09-112">Examples</span></span>


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a><span data-ttu-id="d5d09-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d5d09-113">Requirements</span></span>



| <span data-ttu-id="d5d09-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d5d09-114">Requirement</span></span> | <span data-ttu-id="d5d09-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d5d09-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d5d09-116">Версия</span><span class="sxs-lookup"><span data-stu-id="d5d09-116">Version</span></span><br/> | <span data-ttu-id="d5d09-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="d5d09-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5d09-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5d09-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d09-119">**ЕКУАЛИЗЕРСЕТТИНГС, элемент**</span><span class="sxs-lookup"><span data-stu-id="d5d09-119">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="d5d09-120">**ЕКУАЛИЗЕРСЕТТИНГС. Превиауспресет**</span><span class="sxs-lookup"><span data-stu-id="d5d09-120">**EQUALIZERSETTINGS.previousPreset**</span></span>](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





