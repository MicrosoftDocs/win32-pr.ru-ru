---
description: ICE86 выдает предупреждение, если пакет использует свойство AdminUser в столбце базы данных типа Condition. Авторы пакетов должны использовать привилегированное свойство в условных инструкциях.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25df1e2a9c3ab610e78efd6f797cb916f0563e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347772"
---
# <a name="ice86"></a><span data-ttu-id="c734f-104">ICE86</span><span class="sxs-lookup"><span data-stu-id="c734f-104">ICE86</span></span>

<span data-ttu-id="c734f-105">ICE86 выдает предупреждение, если пакет использует свойство [**AdminUser**](adminuser.md) в столбце базы данных типа [Condition](condition.md) .</span><span class="sxs-lookup"><span data-stu-id="c734f-105">ICE86 issues a warning if the package uses the [**AdminUser**](adminuser.md) property in database column of the [Condition](condition.md) type.</span></span> <span data-ttu-id="c734f-106">Авторы пакетов должны использовать [**привилегированное**](privileged.md) свойство в условных инструкциях.</span><span class="sxs-lookup"><span data-stu-id="c734f-106">Package authors should use the [**Privileged**](privileged.md) property in conditional statements.</span></span>

## <a name="result"></a><span data-ttu-id="c734f-107">Результат</span><span class="sxs-lookup"><span data-stu-id="c734f-107">Result</span></span>

<span data-ttu-id="c734f-108">ICE86 отправляет следующее предупреждение.</span><span class="sxs-lookup"><span data-stu-id="c734f-108">ICE86 posts the following warning.</span></span>



| <span data-ttu-id="c734f-109">Предупреждение ICE86</span><span class="sxs-lookup"><span data-stu-id="c734f-109">ICE86 warning</span></span>                                                                                               | <span data-ttu-id="c734f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c734f-110">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c734f-111">Свойство \` % s \` Найдено в столбце \` % s \` . \` % s \` в строке% s.</span><span class="sxs-lookup"><span data-stu-id="c734f-111">Property \`%s\` found in column \`%s\`.\`%s\` in row %s.</span></span> <span data-ttu-id="c734f-112">\`\`Часто более подходящим является привилегированное свойство.</span><span class="sxs-lookup"><span data-stu-id="c734f-112">\`Privileged\` property is often more appropriate.</span></span> | <span data-ttu-id="c734f-113">В поле условия было использовано свойство [**AdminUser**](adminuser.md) .</span><span class="sxs-lookup"><span data-stu-id="c734f-113">[**AdminUser**](adminuser.md) property was used in a Condition field.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c734f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="c734f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c734f-115">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c734f-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



