---
title: Макросы
description: В подразделах этого раздела приводятся справочные спецификации для сообщений, входящих в указатель, и макросов уведомлений для получения сведений из параметров сообщения ввода указателя.
ms.assetid: 2324DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 07b099a9d0595278e7eb53960da42714763a7f90
ms.sourcegitcommit: f2fe9d9bd65333b74f2af8e30eddbb1643b40c8f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "104412394"
---
# <a name="macros"></a><span data-ttu-id="73d15-103">Макросы</span><span class="sxs-lookup"><span data-stu-id="73d15-103">Macros</span></span>

<span data-ttu-id="73d15-104">В подразделах этого раздела приводятся справочные спецификации для [сообщений, входящих в указатель, и](messages-and-notifications-portal.md) макросов уведомлений для получения сведений из параметров сообщения ввода указателя.</span><span class="sxs-lookup"><span data-stu-id="73d15-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) macros for retrieving information from pointer input message parameters.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="73d15-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="73d15-105">In this section</span></span>



| <span data-ttu-id="73d15-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="73d15-106">Topic</span></span>                                                                                  | <span data-ttu-id="73d15-107">Описание</span><span class="sxs-lookup"><span data-stu-id="73d15-107">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73d15-108">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-108">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                      | <span data-ttu-id="73d15-109">Получает идентификатор указателя, используя указанное значение.</span><span class="sxs-lookup"><span data-stu-id="73d15-109">Retrieves the pointer ID using the specified value.</span></span> <br/>                                                                     |
| [<span data-ttu-id="73d15-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="73d15-111">Проверяет, что указанное сообщение указателя считается намеренным, а не случайным.</span><span class="sxs-lookup"><span data-stu-id="73d15-111">Checks whether the specified pointer message is considered intentional rather than accidental.</span></span><br/>                           |
| [<span data-ttu-id="73d15-112">**IS_POINTER_CANCELED_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-112">**IS_POINTER_CANCELED_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>         | <span data-ttu-id="73d15-113">Проверяет, закончился ли заданный ввод указателя, или он был недопустимым, что указывает на то, что взаимодействие не было завершено.</span><span class="sxs-lookup"><span data-stu-id="73d15-113">Checks whether the specified pointer input ended abruptly, or was invalid, indicating the interaction was not completed.</span></span><br/> |
| [<span data-ttu-id="73d15-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="73d15-115">Проверяет, принял ли указанный указатель пятое действие.</span><span class="sxs-lookup"><span data-stu-id="73d15-115">Checks whether the specified pointer took fifth action.</span></span> <br/>                                                                 |
| [<span data-ttu-id="73d15-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="73d15-117">Проверяет, принял ли указанный указатель первое действие.</span><span class="sxs-lookup"><span data-stu-id="73d15-117">Checks whether the specified pointer took first action.</span></span><br/>                                                                  |
| [<span data-ttu-id="73d15-118">**IS_POINTER_FLAG_SET_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-118">**IS_POINTER_FLAG_SET_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>        | <span data-ttu-id="73d15-119">Проверяет, задает ли макрос указателя указанный флаг.</span><span class="sxs-lookup"><span data-stu-id="73d15-119">Checks whether a pointer macro sets the specified flag.</span></span> <br/>                                                                 |
| [<span data-ttu-id="73d15-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="73d15-121">Проверяет, принял ли указанный указатель четвертое действие.</span><span class="sxs-lookup"><span data-stu-id="73d15-121">Checks whether the specified pointer took fourth action.</span></span> <br/>                                                                |
| [<span data-ttu-id="73d15-122">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-122">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>       | <span data-ttu-id="73d15-123">Проверяет, находится ли указанный указатель в контакте.</span><span class="sxs-lookup"><span data-stu-id="73d15-123">Checks whether the specified pointer is in contact.</span></span> <br/>                                                                     |
| [<span data-ttu-id="73d15-124">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-124">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="73d15-125">Проверяет, находится ли указанный указатель в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="73d15-125">Checks whether the specified pointer is in range.</span></span> <br/>                                                                       |
| [<span data-ttu-id="73d15-126">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-126">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                   | <span data-ttu-id="73d15-127">Проверяет, является ли указанный указатель новым указателем.</span><span class="sxs-lookup"><span data-stu-id="73d15-127">Checks whether the specified pointer is a new pointer.</span></span> <br/>                                                                  |
| [<span data-ttu-id="73d15-128">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-128">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="73d15-129">Проверяет, является ли указанный указатель основным указателем.</span><span class="sxs-lookup"><span data-stu-id="73d15-129">Checks whether the specified pointer is the primary pointer.</span></span> <br/>                                                            |
| [<span data-ttu-id="73d15-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="73d15-131">Проверяет, принял ли указанный указатель второе действие.</span><span class="sxs-lookup"><span data-stu-id="73d15-131">Checks whether the specified pointer took second action.</span></span> <br/>                                                                |
| [<span data-ttu-id="73d15-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="73d15-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="73d15-133">Проверяет, принял ли указанный указатель третье действие.</span><span class="sxs-lookup"><span data-stu-id="73d15-133">Checks whether the specified pointer took third action.</span></span> <br/>                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="73d15-134">См. также</span><span class="sxs-lookup"><span data-stu-id="73d15-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d15-135">Ссылка на входящее сообщение указателя</span><span class="sxs-lookup"><span data-stu-id="73d15-135">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





