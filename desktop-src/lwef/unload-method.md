---
title: Метод выгрузки
description: Метод выгрузки
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790585"
---
# <a name="unload-method"></a><span data-ttu-id="17e13-103">Метод выгрузки</span><span class="sxs-lookup"><span data-stu-id="17e13-103">Unload Method</span></span>

<span data-ttu-id="17e13-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17e13-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="17e13-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="17e13-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="17e13-106">Выгружает символьные данные для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="17e13-106">Unloads the character data for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="17e13-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="17e13-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="17e13-108">*Агент ***. Characters. Unload "*** чарактерид \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="17e13-108">*agent ***.Characters.Unload "*** CharacterID\*\*\*"*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17e13-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17e13-109">Remarks</span></span>

<span data-ttu-id="17e13-110">Используйте этот метод, если символ больше не нужен, чтобы освободить память, используемую для хранения сведений об этом символе.</span><span class="sxs-lookup"><span data-stu-id="17e13-110">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="17e13-111">При повторном доступе к символу используйте метод [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="17e13-111">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

<span data-ttu-id="17e13-112">Этот метод не возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="17e13-112">This method does not return a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 