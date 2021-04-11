---
title: MoveTo, метод
description: MoveTo, метод
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104070005"
---
# <a name="moveto-method"></a><span data-ttu-id="0c493-103">MoveTo, метод</span><span class="sxs-lookup"><span data-stu-id="0c493-103">MoveTo Method</span></span>

<span data-ttu-id="0c493-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c493-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0c493-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="0c493-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0c493-106">Перемещает указанный символ в указанное место.</span><span class="sxs-lookup"><span data-stu-id="0c493-106">Moves the specified character to the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="0c493-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0c493-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0c493-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). MoveTo* \*  *x, y,* \[ *скорость*\]</span><span class="sxs-lookup"><span data-stu-id="0c493-108">*agent ***.Characters ("*** CharacterID\*\*\*").MoveTo*\* *x,y*\[*Speed*\]</span></span>



| <span data-ttu-id="0c493-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="0c493-109">Part</span></span>    | <span data-ttu-id="0c493-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0c493-110">Description</span></span>                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c493-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="0c493-111">*x,y*</span></span>   | <span data-ttu-id="0c493-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0c493-112">Required.</span></span> <span data-ttu-id="0c493-113">Целочисленное значение, указывающее левый край (*x*) и верхний край (*y*) кадра анимации.</span><span class="sxs-lookup"><span data-stu-id="0c493-113">An integer value that indicates the left edge (*x*) and top edge (*y*) of the animation frame.</span></span> <span data-ttu-id="0c493-114">Выражать эти координаты в пикселях.</span><span class="sxs-lookup"><span data-stu-id="0c493-114">Express these coordinates in pixels.</span></span>                                                   |
| <span data-ttu-id="0c493-115">*Скорость*</span><span class="sxs-lookup"><span data-stu-id="0c493-115">*Speed*</span></span> | <span data-ttu-id="0c493-116">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="0c493-116">Optional.</span></span> <span data-ttu-id="0c493-117">Длинное целое число, задающее в миллисекундах скорость перемещения кадра символа.</span><span class="sxs-lookup"><span data-stu-id="0c493-117">A Long integer value specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="0c493-118">Значение по умолчанию ― 1000.</span><span class="sxs-lookup"><span data-stu-id="0c493-118">The default value is 1000.</span></span> <span data-ttu-id="0c493-119">При указании нуля (0) кадр перемещается без воспроизведения анимации.</span><span class="sxs-lookup"><span data-stu-id="0c493-119">Specifying zero (0) moves the frame without playing an animation.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c493-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c493-120">Remarks</span></span>

<span data-ttu-id="0c493-121">Сервер автоматически воспроизводит соответствующую анимацию, назначенную для **перемещаемых** состояний.</span><span class="sxs-lookup"><span data-stu-id="0c493-121">The server automatically plays the appropriate animation assigned to the **Moving** states.</span></span> <span data-ttu-id="0c493-122">Расположение символа основано на левом верхнем углу его фрейма.</span><span class="sxs-lookup"><span data-stu-id="0c493-122">The location of a character is based on the upper left corner of its frame.</span></span>

<span data-ttu-id="0c493-123">Если объявить объектную переменную и задать ее для этого метода, она возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="0c493-123">If you declare an object variable and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="0c493-124">Кроме того, если связанная анимация не загружена на локальный компьютер, сервер устанавливает для свойства [**Status**](status-property.md) объекта **запроса** значение "Failed" (ошибка) с соответствующим номером ошибки.</span><span class="sxs-lookup"><span data-stu-id="0c493-124">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="0c493-125">Поэтому при использовании протокола HTTP для доступа к данным символов или анимации используйте метод [**Get**](get-method.md) для загрузки анимации с **перемещением** состояния перед вызовом метода **MoveTo** .</span><span class="sxs-lookup"><span data-stu-id="0c493-125">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method to load the **Moving** state animations before calling the **MoveTo** method.</span></span>

<span data-ttu-id="0c493-126">Даже если анимация не загружена, сервер по-прежнему перемещает кадр.</span><span class="sxs-lookup"><span data-stu-id="0c493-126">Even if the animation is not loaded, the server still moves the frame.</span></span>

> [!Note]  
> <span data-ttu-id="0c493-127">При вызове **MoveTo** с ненулевым значением перед отображением символа он возвращает состояние сбоя, если ему назначен объект [**запроса**](/windows/desktop/lwef/the-request-object) , поскольку ненулевое значение указывает, что вы пытаетесь воспроизвести анимацию, когда символ не виден.</span><span class="sxs-lookup"><span data-stu-id="0c493-127">If you call **MoveTo** with a nonzero value before the character is shown, it will return a failure status if you assigned it a [**Request**](/windows/desktop/lwef/the-request-object) object, because the nonzero value indicates that you are attempting to play an animation when the character is not visible.</span></span>

 

> [!Note]  
> <span data-ttu-id="0c493-128">Фактический результат параметра *Speed* может меняться в зависимости от скорости процессора компьютера и от приоритета других задач, выполняемых в системе.</span><span class="sxs-lookup"><span data-stu-id="0c493-128">The *Speed* parameter's actual effect may vary based on the speed of the processor of the computer and the priority of other tasks running on the system.</span></span>

 

 

 