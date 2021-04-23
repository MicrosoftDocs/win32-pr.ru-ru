---
description: Действие RegisterUser регистрирует сведения о пользователе с помощью установщика для обнаружения пользователя продукта.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Действие RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813641"
---
# <a name="registeruser-action"></a><span data-ttu-id="1a643-103">Действие RegisterUser</span><span class="sxs-lookup"><span data-stu-id="1a643-103">RegisterUser Action</span></span>

<span data-ttu-id="1a643-104">Действие RegisterUser регистрирует сведения о пользователе с помощью установщика для обнаружения пользователя продукта.</span><span class="sxs-lookup"><span data-stu-id="1a643-104">The RegisterUser action registers the user information with the installer to identify the user of a product.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1a643-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="1a643-105">Sequence Restrictions</span></span>

<span data-ttu-id="1a643-106">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1a643-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1a643-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="1a643-107">ActionData Messages</span></span>



| <span data-ttu-id="1a643-108">Поле</span><span class="sxs-lookup"><span data-stu-id="1a643-108">Field</span></span> | <span data-ttu-id="1a643-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="1a643-109">Description of action data</span></span>   |
|-------|------------------------------|
| <span data-ttu-id="1a643-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1a643-110">\[1\]</span></span> | <span data-ttu-id="1a643-111">Зарегистрированные сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="1a643-111">Registered user information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1a643-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a643-112">Remarks</span></span>

<span data-ttu-id="1a643-113">Действие RegisterUser не выполняется во время административной установки.</span><span class="sxs-lookup"><span data-stu-id="1a643-113">The RegisterUser action is not performed during an administrative installation.</span></span> <span data-ttu-id="1a643-114">Если идентификатор продукта, введенный пользователем, не был проверен [действием валидатепродуктид](validateproductid-action.md), свойство [**ProductID**](productid.md) не задается и это действие не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="1a643-114">If the product identifier entered by the user has not been validated by the [ValidateProductID action](validateproductid-action.md), the [**ProductID**](productid.md) property is not set and this action does nothing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a643-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1a643-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a643-116">**ИМЕН**</span><span class="sxs-lookup"><span data-stu-id="1a643-116">**USERNAME**</span></span>](username.md)
</dt> <dt>

[<span data-ttu-id="1a643-117">**Название**</span><span class="sxs-lookup"><span data-stu-id="1a643-117">**COMPANYNAME**</span></span>](companyname.md)
</dt> <dt>

[<span data-ttu-id="1a643-118">**Кодом**</span><span class="sxs-lookup"><span data-stu-id="1a643-118">**ProductID**</span></span>](productid.md)
</dt> </dl>

 

 



