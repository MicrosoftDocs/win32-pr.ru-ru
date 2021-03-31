---
title: Хасосерклиентс, свойство
description: Хасосерклиентс, свойство
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068004"
---
# <a name="hasotherclients-property"></a><span data-ttu-id="da81e-103">Хасосерклиентс, свойство</span><span class="sxs-lookup"><span data-stu-id="da81e-103">HasOtherClients Property</span></span>

<span data-ttu-id="da81e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="da81e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="da81e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="da81e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="da81e-106">Возвращает значение, указывающее, используется ли указанный символ другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="da81e-106">Returns whether the specified character is in use by other applications.</span></span>

</dd> <dt>

<span data-ttu-id="da81e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="da81e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="da81e-108">*Агент*. **Символы ("***чарактерид***"). Хасосерклиентс**</span><span class="sxs-lookup"><span data-stu-id="da81e-108">*agent*.**Characters("***CharacterID***").HasOtherClients**</span></span>



| <span data-ttu-id="da81e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="da81e-109">Value</span></span>     | <span data-ttu-id="da81e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="da81e-110">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="da81e-111">**True**</span><span class="sxs-lookup"><span data-stu-id="da81e-111">**True**</span></span>  | <span data-ttu-id="da81e-112">Этот символ содержит другие клиенты.</span><span class="sxs-lookup"><span data-stu-id="da81e-112">The character has other clients.</span></span>           |
| <span data-ttu-id="da81e-113">**False**</span><span class="sxs-lookup"><span data-stu-id="da81e-113">**False**</span></span> | <span data-ttu-id="da81e-114">Этот символ не содержит других клиентов.</span><span class="sxs-lookup"><span data-stu-id="da81e-114">The character does not have other clients.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da81e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da81e-115">Remarks</span></span>

<span data-ttu-id="da81e-116">Это свойство можно использовать для определения того, является ли приложение единственным или последним клиентом символа, когда несколько приложений совместно используют один и тот же символ.</span><span class="sxs-lookup"><span data-stu-id="da81e-116">You can use this property to determine whether your application is the only or last client of the character, when more than one application is sharing (has loaded) the same character.</span></span>

 

 




