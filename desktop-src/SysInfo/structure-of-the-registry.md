---
description: Реестр — это иерархическая база данных, которая содержит данные, критически важные для работы Windows и приложений и служб, работающих в Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Структура реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b76b7f827ae3ea96d75d089c7d874c3d31d030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554812"
---
# <a name="structure-of-the-registry"></a><span data-ttu-id="cbd98-103">Структура реестра</span><span class="sxs-lookup"><span data-stu-id="cbd98-103">Structure of the Registry</span></span>

<span data-ttu-id="cbd98-104">Реестр — это иерархическая база данных, которая содержит данные, критически важные для работы Windows и приложений и служб, работающих в Windows.</span><span class="sxs-lookup"><span data-stu-id="cbd98-104">The registry is a hierarchical database that contains data that is critical for the operation of Windows and the applications and services that run on Windows.</span></span> <span data-ttu-id="cbd98-105">Данные структурированы в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="cbd98-105">The data is structured in a tree format.</span></span> <span data-ttu-id="cbd98-106">Каждый узел в дереве называется *ключом*.</span><span class="sxs-lookup"><span data-stu-id="cbd98-106">Each node in the tree is called a *key*.</span></span> <span data-ttu-id="cbd98-107">Каждый ключ может содержать как *подразделы* , так и записи данных, называемые *значениями*.</span><span class="sxs-lookup"><span data-stu-id="cbd98-107">Each key can contain both *subkeys* and data entries called *values*.</span></span> <span data-ttu-id="cbd98-108">Иногда присутствие ключа — это все данные, необходимые приложению. в других случаях приложение открывает ключ и использует значения, связанные с ключом.</span><span class="sxs-lookup"><span data-stu-id="cbd98-108">Sometimes, the presence of a key is all the data that an application requires; other times, an application opens a key and uses the values associated with the key.</span></span> <span data-ttu-id="cbd98-109">Ключ может иметь любое количество значений, а значения могут быть в любой форме.</span><span class="sxs-lookup"><span data-stu-id="cbd98-109">A key can have any number of values, and the values can be in any form.</span></span> <span data-ttu-id="cbd98-110">Дополнительные сведения см. в разделах [типы значений реестра](registry-value-types.md) и [ограничения размера элементов реестра](registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="cbd98-110">For more information, see [Registry Value Types](registry-value-types.md) and [Registry Element Size Limits](registry-element-size-limits.md).</span></span>

<span data-ttu-id="cbd98-111">Каждый ключ имеет имя, состоящее из одного или нескольких печатных символов.</span><span class="sxs-lookup"><span data-stu-id="cbd98-111">Each key has a name consisting of one or more printable characters.</span></span> <span data-ttu-id="cbd98-112">Имена ключей не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="cbd98-112">Key names are not case sensitive.</span></span> <span data-ttu-id="cbd98-113">Имена ключей не могут содержать символ обратной косой черты ( \) , но можно использовать любой другой печатный символ.</span><span class="sxs-lookup"><span data-stu-id="cbd98-113">Key names cannot include the backslash character (\), but any other printable character can be used.</span></span> <span data-ttu-id="cbd98-114">Имена и данные значений могут содержать символ обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="cbd98-114">Value names and data can include the backslash character.</span></span>

<span data-ttu-id="cbd98-115">Имя каждого подраздела уникально по отношению к ключу, расположенному непосредственно над ним в иерархии.</span><span class="sxs-lookup"><span data-stu-id="cbd98-115">The name of each subkey is unique with respect to the key that is immediately above it in the hierarchy.</span></span> <span data-ttu-id="cbd98-116">Имена ключей не локализуются на других языках, хотя значения могут быть.</span><span class="sxs-lookup"><span data-stu-id="cbd98-116">Key names are not localized into other languages, although values may be.</span></span>

<span data-ttu-id="cbd98-117">На следующем рисунке показан пример структуры раздела реестра, отображаемой редактором реестра.</span><span class="sxs-lookup"><span data-stu-id="cbd98-117">The following illustration is an example registry key structure as displayed by the Registry Editor.</span></span>

![окно редактора реестра](images/regtree.png)

<span data-ttu-id="cbd98-119">Каждый из деревьев в разделе **Мой компьютер** является ключом.</span><span class="sxs-lookup"><span data-stu-id="cbd98-119">Each of the trees under **My Computer** is a key.</span></span> <span data-ttu-id="cbd98-120">Ключ **\_ локального \_ компьютера hKey** содержит следующие подразделы: **оборудование**, **SAM**, **Безопасность**, **программное обеспечение** и **система**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-120">The **HKEY\_LOCAL\_MACHINE** key has the following subkeys: **HARDWARE**, **SAM**, **SECURITY**, **SOFTWARE**, and **SYSTEM**.</span></span> <span data-ttu-id="cbd98-121">Каждый из этих ключей, в свою очередь, имеет подразделы.</span><span class="sxs-lookup"><span data-stu-id="cbd98-121">Each of these keys in turn has subkeys.</span></span> <span data-ttu-id="cbd98-122">Например, ключ **оборудования** содержит подразделы **Description**, **девицемап** и **ресаурцемап**; ключ **девицемап** содержит несколько подразделов, включая **видео**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-122">For example, the **HARDWARE** key has the subkeys **DESCRIPTION**, **DEVICEMAP**, and **RESOURCEMAP**; the **DEVICEMAP** key has several subkeys including **VIDEO**.</span></span>

<span data-ttu-id="cbd98-123">Каждое значение состоит из имени значения и связанных с ним данных, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="cbd98-123">Each value consists of a value name and its associated data, if any.</span></span> <span data-ttu-id="cbd98-124">**Максобжектнумбер** и **вгакомпатибле** — это значения, которые содержат данные в подразделе **видео** .</span><span class="sxs-lookup"><span data-stu-id="cbd98-124">**MaxObjectNumber** and **VgaCompatible** are values that contain data under the **VIDEO** subkey.</span></span>

<span data-ttu-id="cbd98-125">Дерево реестра может иметь глубину 512 уровней.</span><span class="sxs-lookup"><span data-stu-id="cbd98-125">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="cbd98-126">С помощью одного вызова API реестра можно создать до 32 уровней за раз.</span><span class="sxs-lookup"><span data-stu-id="cbd98-126">You can create up to 32 levels at a time through a single registry API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbd98-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cbd98-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cbd98-128">[Общие сведения о реестре Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="cbd98-128">[Overview of the Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span></span>
</dt> </dl>

 

 
