---
description: Действие Валидатепродуктид задает для свойства ProductID полный идентификатор продукта.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Действие Валидатепродуктид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650573"
---
# <a name="validateproductid-action"></a><span data-ttu-id="0e98f-103">Действие Валидатепродуктид</span><span class="sxs-lookup"><span data-stu-id="0e98f-103">ValidateProductID Action</span></span>

<span data-ttu-id="0e98f-104">Действие Валидатепродуктид задает для свойства [**ProductID**](productid.md) полный идентификатор продукта.</span><span class="sxs-lookup"><span data-stu-id="0e98f-104">The ValidateProductID action sets the [**ProductID**](productid.md) property to the full product identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0e98f-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="0e98f-105">Sequence Restrictions</span></span>

<span data-ttu-id="0e98f-106">Это действие должно быть упорядочено перед мастером пользовательского интерфейса в [таблице инсталлуисекуенце](installuisequence-table.md) и перед [действием RegisterUser](registeruser-action.md) в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="0e98f-106">This action must be sequenced before the user interface wizard in the [InstallUISequence table](installuisequence-table.md) and before the [RegisterUser action](registeruser-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0e98f-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="0e98f-107">ActionData Messages</span></span>

<span data-ttu-id="0e98f-108">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="0e98f-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e98f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e98f-109">Remarks</span></span>

<span data-ttu-id="0e98f-110">Установщик проверяет успешность проверки продукта, проверяя свойство [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="0e98f-110">The installer checks whether a product has validated successfully by checking the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="0e98f-111">Установщик присваивает свойству **ProductID** полный идентификатор продукта после успешной проверки.</span><span class="sxs-lookup"><span data-stu-id="0e98f-111">The installer sets the **ProductID** property to the full product identifier after a successful validation.</span></span> <span data-ttu-id="0e98f-112">Действие Валидатепродуктид не выполняет никаких действий, если свойство **ProductID** уже было задано успешной проверкой или другим методом.</span><span class="sxs-lookup"><span data-stu-id="0e98f-112">The ValidateProductID action does nothing if the **ProductID** property has already been set by a successful validation or by another method.</span></span>

<span data-ttu-id="0e98f-113">Действие Валидатепродуктид всегда возвращает значение Success, независимо от того, является ли идентификатор продукта допустимым, чтобы идентификатор продукта можно было указать в командной строке при первом запуске продукта.</span><span class="sxs-lookup"><span data-stu-id="0e98f-113">The ValidateProductID action always returns a success, whether or not the product identifier is valid, so that the product identifier can be entered on the command line the first time the product is run.</span></span>

<span data-ttu-id="0e98f-114">Идентификатор продукта может быть проверен без необходимости повторного ввода этих данных пользователем путем задания свойства [**PIDKEY**](pidkey.md) в командной строке или при помощи преобразования.</span><span class="sxs-lookup"><span data-stu-id="0e98f-114">The product identifier can be validated without having the user reenter this information by setting the [**PIDKEY**](pidkey.md) property on the command line or by using a transform.</span></span> <span data-ttu-id="0e98f-115">После этого диалоговое окно, запрашивающее пользователя ввести идентификатор продукта, может быть условным на наличие свойства [**ProductID**](productid.md) , которое задается при проверке свойства **PIDKEY** .</span><span class="sxs-lookup"><span data-stu-id="0e98f-115">The display of the dialog box requesting the user to enter the product identifier can then be made conditional upon the presence of the [**ProductID**](productid.md) property, which is set when the **PIDKEY** property is validated.</span></span>

 

 



