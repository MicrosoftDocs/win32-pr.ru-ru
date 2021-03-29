---
title: Раисерекуестеррорс, свойство
description: Раисерекуестеррорс, свойство
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260844"
---
# <a name="raiserequesterrors-property"></a><span data-ttu-id="aab25-103">Раисерекуестеррорс, свойство</span><span class="sxs-lookup"><span data-stu-id="aab25-103">RaiseRequestErrors Property</span></span>

<span data-ttu-id="aab25-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aab25-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="aab25-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="aab25-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="aab25-106">Возвращает или задает значение, указывающее, вызываются ли ошибки для запросов.</span><span class="sxs-lookup"><span data-stu-id="aab25-106">Returns or sets whether errors for requests are raised.</span></span>

</dd> <dt>

<span data-ttu-id="aab25-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="aab25-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="aab25-108">\*агент \* \* *. Раисерекуестеррорс* \*  \[  =  *Boolean*\]</span><span class="sxs-lookup"><span data-stu-id="aab25-108">*agent\*\*\*.RaiseRequestErrors*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="aab25-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="aab25-109">Part</span></span>      | <span data-ttu-id="aab25-110">Описание</span><span class="sxs-lookup"><span data-stu-id="aab25-110">Description</span></span>                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aab25-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="aab25-111">*boolean*</span></span> | <span data-ttu-id="aab25-112">Логическое значение, определяющее, вызываются ли ошибки в запросах.</span><span class="sxs-lookup"><span data-stu-id="aab25-112">A Boolean value that determines whether errors in requests are raised.</span></span><br/> <span data-ttu-id="aab25-113">Возникнет ошибка запроса **true** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="aab25-113">**True**    (Default) Request errors are raised.</span></span> <br/> <span data-ttu-id="aab25-114">**Значение false**     Ошибки запросов не вызываются.</span><span class="sxs-lookup"><span data-stu-id="aab25-114">**False**     Request errors are not raised.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aab25-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aab25-115">Remarks</span></span>

<span data-ttu-id="aab25-116">Это свойство позволяет определить, вызывает ли сервер ошибки, происходящие с методами, поддерживающими объекты [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="aab25-116">This property enables you to determine whether the server raises errors that occur with methods that support [**Request**](/windows/desktop/lwef/the-request-object) objects.</span></span> <span data-ttu-id="aab25-117">Например, если указать имя анимации, которое не существует в методе [**Play**](play-method.md), сервер выдает ошибку (отображается сообщение об ошибке), если для этого свойства не задано **значение false**.</span><span class="sxs-lookup"><span data-stu-id="aab25-117">For example, if you specify an animation name that does not exist in a [**Play**](play-method.md)method, the server raises an error (displaying the error message) unless you set this property to **False**.</span></span>

<span data-ttu-id="aab25-118">Он может быть полезен для языков программирования, которые не обеспечивают восстановление при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="aab25-118">It may be useful for programming languages that do not provide recovery when an error is raised.</span></span> <span data-ttu-id="aab25-119">Однако при установке этого свойства в **значение false** следует соблюдать осторожность, так как может оказаться труднее обнаружить ошибки в коде.</span><span class="sxs-lookup"><span data-stu-id="aab25-119">However, use care when setting this property to **False**, because it might be harder to find errors in your code.</span></span>

 

