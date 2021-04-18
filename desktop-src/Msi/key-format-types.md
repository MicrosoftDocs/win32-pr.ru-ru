---
description: Типы форматов ключей настраиваемых данных могут использоваться в текстовых полях для предоставления ключа в таблицу базы данных.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Типы форматов ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682711"
---
# <a name="key-format-types"></a><span data-ttu-id="ea91e-103">Типы форматов ключей</span><span class="sxs-lookup"><span data-stu-id="ea91e-103">Key Format Types</span></span>

<span data-ttu-id="ea91e-104">Типы форматов ключей настраиваемых данных могут использоваться в текстовых полях для предоставления ключа в таблицу базы данных.</span><span class="sxs-lookup"><span data-stu-id="ea91e-104">The Key Format Types of configurable data may be used in text fields to provide a key into a database table.</span></span> <span data-ttu-id="ea91e-105">Атрибут Мсмконфигитемноннуллабле является неявным в этом формате данных и не требует установки.</span><span class="sxs-lookup"><span data-stu-id="ea91e-105">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="ea91e-106">Значение NULL никогда не является допустимым значением для этого типа.</span><span class="sxs-lookup"><span data-stu-id="ea91e-106">Null is never a valid value for this type.</span></span> <span data-ttu-id="ea91e-107">Ответы на все элементы формата ключа должны быть в [специальном формате кмсм](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="ea91e-107">Responses to all Key format items must be in [CMSM Special Format](cmsm-special-format.md).</span></span>

<span data-ttu-id="ea91e-108">Существуют следующие типы форматов ключей:</span><span class="sxs-lookup"><span data-stu-id="ea91e-108">The following Key Format types exist:</span></span>

[<span data-ttu-id="ea91e-109">Тип каталога</span><span class="sxs-lookup"><span data-stu-id="ea91e-109">Directory Type</span></span>](directory-type.md)

[<span data-ttu-id="ea91e-110">Тип файла</span><span class="sxs-lookup"><span data-stu-id="ea91e-110">File Type</span></span>](file-type.md)

[<span data-ttu-id="ea91e-111">Тип свойства</span><span class="sxs-lookup"><span data-stu-id="ea91e-111">Property Type</span></span>](property-type.md)

[<span data-ttu-id="ea91e-112">Тип диалогового окна</span><span class="sxs-lookup"><span data-stu-id="ea91e-112">Dialog Type</span></span>](dialog-type.md)

[<span data-ttu-id="ea91e-113">Двоичный тип</span><span class="sxs-lookup"><span data-stu-id="ea91e-113">Binary Type</span></span>](binary-type.md)

[<span data-ttu-id="ea91e-114">Тип значка</span><span class="sxs-lookup"><span data-stu-id="ea91e-114">Icon Type</span></span>](icon-type.md)

<span data-ttu-id="ea91e-115">Настраиваемые элементы типа формата ключа используются в текстовых столбцах для предоставления ключа базы данных, а в целом можно заменить любой текстовой строкой.</span><span class="sxs-lookup"><span data-stu-id="ea91e-115">Configurable items of the Key Format Type are used in text columns to provide a database key and in general could be replaced by any text string.</span></span> <span data-ttu-id="ea91e-116">Отдельные типы могут иметь дополнительные синтаксические ограничения, но эти ограничения не применяются Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="ea91e-116">The individual types may have additional syntactic restrictions, but these restrictions are not enforced by Mergemod.dll.</span></span> <span data-ttu-id="ea91e-117">Определенные настраиваемые элементы также могут иметь ограничения семантики характеристик.</span><span class="sxs-lookup"><span data-stu-id="ea91e-117">Particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="ea91e-118">Например, конкретный настраиваемый элемент может быть ключом к [двоичной таблице](binary-table.md) в строке, содержащей растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="ea91e-118">For example, a particular configurable item may be required to be a key into the [Binary table](binary-table.md) to a row containing a bitmap image.</span></span> <span data-ttu-id="ea91e-119">Такие ограничения не применяются Mergemod.dll, поэтому авторы модулей должны быть готовы к обработке любой строки, удовлетворяющей заданному типу формата ключа.</span><span class="sxs-lookup"><span data-stu-id="ea91e-119">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Key Format type.</span></span> <span data-ttu-id="ea91e-120">Если иное не указано семантическим значением или атрибутами, значение null является допустимым ответом.</span><span class="sxs-lookup"><span data-stu-id="ea91e-120">Unless otherwise specified by semantic meaning or attributes, null is a valid response.</span></span>

 

 



