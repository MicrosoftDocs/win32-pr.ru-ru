---
title: Элементы управления. доступно
description: Свойство Available указывает, доступен ли указанный тип сведений, или может быть выполнено указанное действие. | Элементы управления. доступно
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Универсальный проигрыватель Windows Media Controls.
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698763"
---
# <a name="controlsisavailable"></a><span data-ttu-id="b947c-105">Элементы управления. доступно</span><span class="sxs-lookup"><span data-stu-id="b947c-105">Controls.isAvailable</span></span>

<span data-ttu-id="b947c-106">Свойство **Available** указывает, доступен ли указанный тип сведений, или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="b947c-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="b947c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b947c-107">Parameters</span></span>

<span data-ttu-id="b947c-108">*name*</span><span class="sxs-lookup"><span data-stu-id="b947c-108">*name*</span></span>

<span data-ttu-id="b947c-109">**Строка** , содержащая одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b947c-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="b947c-110">Строка</span><span class="sxs-lookup"><span data-stu-id="b947c-110">String</span></span>          | <span data-ttu-id="b947c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b947c-111">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b947c-112">currentItem</span><span class="sxs-lookup"><span data-stu-id="b947c-112">currentItem</span></span>     | <span data-ttu-id="b947c-113">Определяет, может ли пользователь задать свойство **currentItem** .</span><span class="sxs-lookup"><span data-stu-id="b947c-113">Determines whether the user can set the **currentItem** property.</span></span>                                                                                                 |
| <span data-ttu-id="b947c-114">куррентмаркер</span><span class="sxs-lookup"><span data-stu-id="b947c-114">currentMarker</span></span>   | <span data-ttu-id="b947c-115">Определяет, может ли пользователь выполнять поиск определенного маркера.</span><span class="sxs-lookup"><span data-stu-id="b947c-115">Determines whether the user can seek to a specific marker.</span></span>                                                                                                        |
| <span data-ttu-id="b947c-116">currentPosition</span><span class="sxs-lookup"><span data-stu-id="b947c-116">currentPosition</span></span> | <span data-ttu-id="b947c-117">Определяет, может ли пользователь искать определенную точку в файле.</span><span class="sxs-lookup"><span data-stu-id="b947c-117">Determines whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="b947c-118">Некоторые файлы не поддерживают поиск.</span><span class="sxs-lookup"><span data-stu-id="b947c-118">Some files do not support seeking.</span></span>                                                       |
| <span data-ttu-id="b947c-119">фастфорвард</span><span class="sxs-lookup"><span data-stu-id="b947c-119">fastForward</span></span>     | <span data-ttu-id="b947c-120">Определяет, поддерживает ли файл быструю пересылку и можно ли вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b947c-120">Determines whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="b947c-121">Многие типы файлов (или динамические потоки) не поддерживают Фастфорвард.</span><span class="sxs-lookup"><span data-stu-id="b947c-121">Many file types (or live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="b947c-122">фастреверсе</span><span class="sxs-lookup"><span data-stu-id="b947c-122">fastReverse</span></span>     | <span data-ttu-id="b947c-123">Определяет, поддерживает ли файл Фастреверсе и можно ли вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b947c-123">Determines whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="b947c-124">Многие типы файлов (или динамические потоки) не поддерживают Фастреверсе.</span><span class="sxs-lookup"><span data-stu-id="b947c-124">Many file types (or live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="b947c-125">Далее</span><span class="sxs-lookup"><span data-stu-id="b947c-125">next</span></span>            | <span data-ttu-id="b947c-126">Определяет, может ли пользователь перейти к следующей записи списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b947c-126">Determines whether the user can seek to the next entry in a playlist.</span></span>                                                                                             |
| <span data-ttu-id="b947c-127">pause</span><span class="sxs-lookup"><span data-stu-id="b947c-127">pause</span></span>           | <span data-ttu-id="b947c-128">Определяет, доступен ли метод **Pause** .</span><span class="sxs-lookup"><span data-stu-id="b947c-128">Determines whether the **pause** method is available.</span></span>                                                                                                             |
| <span data-ttu-id="b947c-129">играть</span><span class="sxs-lookup"><span data-stu-id="b947c-129">play</span></span>            | <span data-ttu-id="b947c-130">Определяет, доступен ли метод **Play** .</span><span class="sxs-lookup"><span data-stu-id="b947c-130">Determines whether the **play** method is available.</span></span>                                                                                                              |
| <span data-ttu-id="b947c-131">Предыдущее время</span><span class="sxs-lookup"><span data-stu-id="b947c-131">previous</span></span>        | <span data-ttu-id="b947c-132">Определяет, может ли пользователь перейти к предыдущей записи списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b947c-132">Determines whether the user can seek to the previous entry in a playlist.</span></span>                                                                                         |
| <span data-ttu-id="b947c-133">Шаг</span><span class="sxs-lookup"><span data-stu-id="b947c-133">step</span></span>            | <span data-ttu-id="b947c-134">Определяет, доступен ли метод **Step** во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b947c-134">Determines whether the **step** method is available during playback.</span></span>                                                                                              |
| <span data-ttu-id="b947c-135">stop</span><span class="sxs-lookup"><span data-stu-id="b947c-135">stop</span></span>            | <span data-ttu-id="b947c-136">Определяет, доступен ли метод " **останавливаться** ".</span><span class="sxs-lookup"><span data-stu-id="b947c-136">Determines whether the **stop** method is available.</span></span>                                                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="b947c-137">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b947c-137">Return Values</span></span>

<span data-ttu-id="b947c-138">Этот метод возвращает **логическое** значение.</span><span class="sxs-lookup"><span data-stu-id="b947c-138">This method returns a **Boolean** value.</span></span>

## <a name="examples"></a><span data-ttu-id="b947c-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="b947c-139">Examples</span></span>

<span data-ttu-id="b947c-140">В следующем примере создается HTML-элемент BUTTON, который выполняет поиск начальной позиции текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b947c-140">The following example creates an HTML BUTTON element that seeks to the starting position of the current media item.</span></span> <span data-ttu-id="b947c-141">В коде JScript для проверки того, поддерживает ли файл операцию поиска **, можно использовать** параметр.</span><span class="sxs-lookup"><span data-stu-id="b947c-141">The JScript code uses **isAvailable** to verify that the file supports the seek operation.</span></span> <span data-ttu-id="b947c-142">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="b947c-142">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a><span data-ttu-id="b947c-143">Требования</span><span class="sxs-lookup"><span data-stu-id="b947c-143">Requirements</span></span>



| <span data-ttu-id="b947c-144">Требование</span><span class="sxs-lookup"><span data-stu-id="b947c-144">Requirement</span></span> | <span data-ttu-id="b947c-145">Значение</span><span class="sxs-lookup"><span data-stu-id="b947c-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b947c-146">Версия</span><span class="sxs-lookup"><span data-stu-id="b947c-146">Version</span></span><br/> | <span data-ttu-id="b947c-147">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b947c-147">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="b947c-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b947c-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="b947c-149"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b947c-149"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b947c-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b947c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b947c-151">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="b947c-151">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





