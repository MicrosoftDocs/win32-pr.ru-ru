---
title: Метод отображения
description: Метод отображения
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700844"
---
# <a name="show-method"></a><span data-ttu-id="88258-103">Метод отображения</span><span class="sxs-lookup"><span data-stu-id="88258-103">Show Method</span></span>

<span data-ttu-id="88258-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="88258-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="88258-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="88258-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="88258-106">Делает указанный символ видимым и воспроизводит **его связанную** анимацию.</span><span class="sxs-lookup"><span data-stu-id="88258-106">Makes the specified character visible and plays its associated **Showing** animation.</span></span>

</dd> <dt>

<span data-ttu-id="88258-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="88258-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="88258-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Показывать* \*  \[ *быстро*\]</span><span class="sxs-lookup"><span data-stu-id="88258-108">*agent ***.Characters ("*** CharacterID\*\*\*").Show*\* \[*Fast*\]</span></span>



| <span data-ttu-id="88258-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="88258-109">Part</span></span>   | <span data-ttu-id="88258-110">Описание</span><span class="sxs-lookup"><span data-stu-id="88258-110">Description</span></span>                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88258-111">*Быстрый*</span><span class="sxs-lookup"><span data-stu-id="88258-111">*Fast*</span></span> | <span data-ttu-id="88258-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="88258-112">Optional.</span></span> <span data-ttu-id="88258-113">Логическое выражение, указывающее, воспроизводит ли сервер **отображаемую** анимацию.</span><span class="sxs-lookup"><span data-stu-id="88258-113">A Boolean expression specifying whether the server plays the **Showing** animation.</span></span> <span data-ttu-id="88258-114">**Значение true** Пропускает **отображаемую** анимацию состояния.</span><span class="sxs-lookup"><span data-stu-id="88258-114">**True** Skips the **Showing** state animation.</span></span> <br/> <span data-ttu-id="88258-115">**Значение false** (по умолчанию) не пропускает анимацию **отображаемого** состояния.</span><span class="sxs-lookup"><span data-stu-id="88258-115">**False** (Default) Does not skip the **Showing** state animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88258-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88258-116">Remarks</span></span>

<span data-ttu-id="88258-117">Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="88258-117">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="88258-118">Кроме того, если связанная **анимация с** анимацией не была загружена и параметр **быстрого** параметра не был задан как **true**, сервер устанавливает для свойства [**Status**](status-property.md) объекта **запроса** значение "сбой" с соответствующим номером ошибки.</span><span class="sxs-lookup"><span data-stu-id="88258-118">In addition, if the associated **Showing** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="88258-119">Поэтому, если для доступа к данным символьной анимации используется протокол HTTP, перед вызовом метода **Показать** используйте метод [**Get**](get-method.md) , чтобы загрузить анимацию с **отображением** состояния.</span><span class="sxs-lookup"><span data-stu-id="88258-119">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Showing** state animation before calling the **Show** method.</span></span>

<span data-ttu-id="88258-120">Старайтесь не задавать  для параметра fast **значение true** без предварительного воспроизведения анимации. в противном случае символьная рамка может отображаться без изображения.</span><span class="sxs-lookup"><span data-stu-id="88258-120">Avoid setting the **Fast** parameter to **True** without first playing an animation beforehand; otherwise, the character frame may display with no image.</span></span> <span data-ttu-id="88258-121">В частности, обратите внимание, что при вызове функции [**MoveTo**](moveto-method.md) , если символ не отображается, анимация не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="88258-121">In particular, note that if you call [**MoveTo**](moveto-method.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="88258-122">Таким образом, при вызове метода **Показать** с **быстрым** установленным значение **true** изображение не отображается.</span><span class="sxs-lookup"><span data-stu-id="88258-122">Therefore, if you call the **Show** method with **Fast** set to **True**, no image will display.</span></span> <span data-ttu-id="88258-123">Аналогично, если вызвать [**Hide**](hide-method.md) , а затем **Показать** с параметром **быстрое** задание в **значение true**, изображение не будет отображено.</span><span class="sxs-lookup"><span data-stu-id="88258-123">Similarly, if you call [**Hide**](hide-method.md) then **Show** with **Fast** set to **True**, there will be no visible image.</span></span>

## <a name="see-also"></a><span data-ttu-id="88258-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="88258-124">See Also</span></span>

[<span data-ttu-id="88258-125">**Hide - метод**</span><span class="sxs-lookup"><span data-stu-id="88258-125">**Hide method**</span></span>](hide-method.md)


 

