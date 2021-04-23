---
title: Удалить метод
description: Удалить метод
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337476"
---
# <a name="remove-method"></a><span data-ttu-id="35c96-103">Удалить метод</span><span class="sxs-lookup"><span data-stu-id="35c96-103">Remove Method</span></span>

<span data-ttu-id="35c96-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="35c96-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="35c96-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="35c96-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="35c96-106">Удаляет объект [**Command**](/windows/desktop/lwef/the-command-object) из коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="35c96-106">Removes a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="35c96-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="35c96-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="35c96-108">*Агент ***. Символы ("*** чарактерид ***"). Команды. удалить*** имя*</span><span class="sxs-lookup"><span data-stu-id="35c96-108">*agent ***.Characters ("*** CharacterID ***").Commands.Remove*** Name*</span></span>



| <span data-ttu-id="35c96-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="35c96-109">Part</span></span>   | <span data-ttu-id="35c96-110">Описание</span><span class="sxs-lookup"><span data-stu-id="35c96-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="35c96-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="35c96-111">*Name*</span></span> | <span data-ttu-id="35c96-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="35c96-112">Required.</span></span> <span data-ttu-id="35c96-113">Строковое значение, соответствующее ИДЕНТИФИКАТОРу команды.</span><span class="sxs-lookup"><span data-stu-id="35c96-113">A string value corresponding to the ID for the command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35c96-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35c96-114">Remarks</span></span>

<span data-ttu-id="35c96-115">Когда объект [**Command**](/windows/desktop/lwef/the-command-object) удаляется из коллекции, он больше не отображается при отображении всплывающего меню символа или в окне команды, если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="35c96-115">When a [**Command**](/windows/desktop/lwef/the-command-object) object is removed from the collection, it no longer appears when the character's pop-up menu is displayed or in the Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="35c96-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="35c96-116">See Also</span></span>

[<span data-ttu-id="35c96-117">**RemoveAll, метод**</span><span class="sxs-lookup"><span data-stu-id="35c96-117">**RemoveAll method**</span></span>](removeall-method.md)


 

 