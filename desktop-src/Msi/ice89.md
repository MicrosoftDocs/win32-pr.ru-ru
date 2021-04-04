---
description: ICE89 проверяет, что значение в \_ родительском столбце ProgID в таблице ProgID является допустимым внешним ключом в столбце ProgID в таблице ProgID. Каждый родительский элемент ProgId должен иметь запись в таблице ProgId.
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d14ec5b17a20b9046625feb464865bd0c08419e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999241"
---
# <a name="ice89"></a><span data-ttu-id="c9b9e-104">ICE89</span><span class="sxs-lookup"><span data-stu-id="c9b9e-104">ICE89</span></span>

<span data-ttu-id="c9b9e-105">ICE89 проверяет, что значение в \_ родительском столбце ProgID в [таблице ProgID](progid-table.md) является допустимым внешним ключом в столбце ProgId в таблице ProgID.</span><span class="sxs-lookup"><span data-stu-id="c9b9e-105">ICE89 validates that the value in the Progid\_Parent column in [ProgId table](progid-table.md) is a valid foreign key into the ProgId column in ProgId table.</span></span> <span data-ttu-id="c9b9e-106">Каждый родительский элемент ProgId должен иметь запись в таблице ProgId.</span><span class="sxs-lookup"><span data-stu-id="c9b9e-106">Every ProgId parent should have a record in the ProgId table.</span></span>

## <a name="result"></a><span data-ttu-id="c9b9e-107">Результат</span><span class="sxs-lookup"><span data-stu-id="c9b9e-107">Result</span></span>

<span data-ttu-id="c9b9e-108">ICE89 отправляет следующие ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9b9e-108">ICE89 posts the following errors.</span></span>



| <span data-ttu-id="c9b9e-109">ICE89, ошибка</span><span class="sxs-lookup"><span data-stu-id="c9b9e-109">ICE89 error</span></span>                                                           | <span data-ttu-id="c9b9e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c9b9e-110">Description</span></span>                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="c9b9e-111">\_Родительский идентификатор ProgID " \[ 1 \] " в таблице ProgID не является допустимым ProgID.</span><span class="sxs-lookup"><span data-stu-id="c9b9e-111">The ProgId\_Parent '\[1\]' in the ProgId table is not a valid ProgId.</span></span> | <span data-ttu-id="c9b9e-112">Указан родительский идентификатор ProgId, не указанный в таблице ProgId.</span><span class="sxs-lookup"><span data-stu-id="c9b9e-112">There is a ProgId parent specified that is not listed in the ProgId table.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c9b9e-113">См. также</span><span class="sxs-lookup"><span data-stu-id="c9b9e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9b9e-114">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c9b9e-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



