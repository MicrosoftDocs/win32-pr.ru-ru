---
title: Метод Жестуреат
description: Метод Жестуреат
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487564"
---
# <a name="gestureat-method"></a><span data-ttu-id="40aa1-103">Метод Жестуреат</span><span class="sxs-lookup"><span data-stu-id="40aa1-103">GestureAt Method</span></span>

<span data-ttu-id="40aa1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="40aa1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="40aa1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="40aa1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="40aa1-106">Воспроизводит анимацию жестуринг для указанного символа в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="40aa1-106">Plays the gesturing animation for the specified character at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="40aa1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="40aa1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="40aa1-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Жестуреат* \*  *x, y*</span><span class="sxs-lookup"><span data-stu-id="40aa1-108">*agent ***.Characters ("*** CharacterID\*\*\*").GestureAt*\* *x,y*</span></span>



| <span data-ttu-id="40aa1-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="40aa1-109">Part</span></span>  | <span data-ttu-id="40aa1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="40aa1-110">Description</span></span>                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40aa1-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="40aa1-111">*x,y*</span></span> | <span data-ttu-id="40aa1-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="40aa1-112">Required.</span></span> <span data-ttu-id="40aa1-113">Целочисленное значение, указывающее горизонтальную (*x*) координату экрана и координату по вертикали (*y*), на которую будет заменяться символ.</span><span class="sxs-lookup"><span data-stu-id="40aa1-113">An integer value that indicates the horizontal (*x*) screen coordinate and vertical (*y*) screen coordinate to which the character will gesture.</span></span> <span data-ttu-id="40aa1-114">Эти координаты должны быть указаны в пикселях.</span><span class="sxs-lookup"><span data-stu-id="40aa1-114">These coordinates must be specified in pixels.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40aa1-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40aa1-115">Remarks</span></span>

<span data-ttu-id="40aa1-116">Сервер автоматически воспроизводит соответствующую анимацию, чтобы выполнить жест в направлении к указанному расположению.</span><span class="sxs-lookup"><span data-stu-id="40aa1-116">The server automatically plays the appropriate animation to gesture toward the specified location.</span></span> <span data-ttu-id="40aa1-117">Координаты всегда зависят от источника экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="40aa1-117">The coordinates are always relative to the screen origin (upper left).</span></span>

<span data-ttu-id="40aa1-118">Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="40aa1-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="40aa1-119">Кроме того, если связанная анимация не загружена на локальный компьютер, сервер устанавливает для свойства [**Status**](status-property.md) объекта **запроса** значение "Failed" (ошибка) с соответствующим номером ошибки.</span><span class="sxs-lookup"><span data-stu-id="40aa1-119">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="40aa1-120">Поэтому при использовании протокола HTTP для доступа к данным анимации символов используйте метод [**Get**](get-method.md) для загрузки анимации состояния **жестуринг** перед вызовом метода **жестуреат** .</span><span class="sxs-lookup"><span data-stu-id="40aa1-120">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Gesturing** state animations before calling the **GestureAt** method.</span></span>

 

 