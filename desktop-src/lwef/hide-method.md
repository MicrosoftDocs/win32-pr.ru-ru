---
title: Hide, метод
description: Hide, метод
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133799"
---
# <a name="hide-method"></a><span data-ttu-id="6fb24-103">Hide, метод</span><span class="sxs-lookup"><span data-stu-id="6fb24-103">Hide Method</span></span>

<span data-ttu-id="6fb24-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6fb24-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6fb24-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="6fb24-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6fb24-106">Скрывает указанный символ.</span><span class="sxs-lookup"><span data-stu-id="6fb24-106">Hides the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="6fb24-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6fb24-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6fb24-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Скрыть* \*  \[ *быстрое*\]</span><span class="sxs-lookup"><span data-stu-id="6fb24-108">*agent ***.Characters ("*** CharacterID\*\*\*").Hide*\* \[*Fast*\]</span></span>



| <span data-ttu-id="6fb24-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="6fb24-109">Part</span></span>   | <span data-ttu-id="6fb24-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6fb24-110">Description</span></span>                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb24-111">*Быстрый*</span><span class="sxs-lookup"><span data-stu-id="6fb24-111">*Fast*</span></span> | <span data-ttu-id="6fb24-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6fb24-112">Optional.</span></span> <span data-ttu-id="6fb24-113">Логическое значение, указывающее, следует ли пропустить анимацию, связанную с состоянием скрытия символа **true** , не воспроизводит анимацию **скрытия** .</span><span class="sxs-lookup"><span data-stu-id="6fb24-113">A Boolean value that indicates whether to skip the animation associated with the character's Hiding state **True** Does not play the **Hiding** animation.</span></span> <br/> <span data-ttu-id="6fb24-114">**False** (по умолчанию) воспроизводит анимацию **скрытия** .</span><span class="sxs-lookup"><span data-stu-id="6fb24-114">**False** (Default) Plays the **Hiding** animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fb24-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6fb24-115">Remarks</span></span>

<span data-ttu-id="6fb24-116">Сервер помещает в очередь действия метода **Hide** в очереди символов, поэтому его можно использовать для скрытия символа после последовательности других анимаций.</span><span class="sxs-lookup"><span data-stu-id="6fb24-116">The server queues the actions of the **Hide** method in the character's queue, so you can use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="6fb24-117">Вы можете воспроизвести действие немедленно, используя метод " [**останавливаться**](stop-method.md) " перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="6fb24-117">You can play the action immediately by using the [**Stop**](stop-method.md) method before calling this method.</span></span>

<span data-ttu-id="6fb24-118">Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="6fb24-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="6fb24-119">Кроме того, если связанная **Скрытая** анимация не была загружена и параметр **fast** не был задан как **true**, сервер устанавливает для свойства [**состояние**](status-property.md) объекта **запроса** значение "сбой" с соответствующим номером ошибки.</span><span class="sxs-lookup"><span data-stu-id="6fb24-119">In addition, if the associated **Hiding** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="6fb24-120">Поэтому при использовании протокола HTTP для доступа к данным символов или анимации используйте метод [**Get**](get-method.md) и укажите состояние **скрытия** , чтобы загрузить анимацию перед вызовом метода **Hide** .</span><span class="sxs-lookup"><span data-stu-id="6fb24-120">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method and specify the **Hiding** state to load the animation before calling the **Hide** method.</span></span>

<span data-ttu-id="6fb24-121">Скрытие символа может также привести к срабатыванию события [**активатеинпут**](activateinput-event.md) другого клиента.</span><span class="sxs-lookup"><span data-stu-id="6fb24-121">Hiding a character can also result in triggering the [**ActivateInput**](activateinput-event.md) event of another client.</span></span>

> [!Note]  
> <span data-ttu-id="6fb24-122">Скрытые символы не могут получить доступ к каналу аудио.</span><span class="sxs-lookup"><span data-stu-id="6fb24-122">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="6fb24-123">Сервер передаст состояние сбоя в событии [**рекуесткомплете**](requestcomplete-event.md) , если создается запрос анимации и этот символ скрыт.</span><span class="sxs-lookup"><span data-stu-id="6fb24-123">The server will pass back a failure status in the [**RequestComplete**](requestcomplete-event.md) event if you generate an animation request and the character is hidden.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6fb24-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="6fb24-124">See Also</span></span>

[<span data-ttu-id="6fb24-125">**Show - метод**</span><span class="sxs-lookup"><span data-stu-id="6fb24-125">**Show method**</span></span>](show-method.md)


 

